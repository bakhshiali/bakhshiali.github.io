---
title: "Chatbot"
collection: projects
type: "Undergraduate projects"
permalink: /projects/Chatbot
venue: "Tabriz"
date: 2016-1-1
location: "Tabriz, Iran"
---

<h2>What is Chatbot?</h2>

<p align="justify" style="padding-left: 1em">A chatbot (also known as a smartbot, talkbot, chatterbot, Bot, IM bot, interactive agent, Conversational interface or Artificial Conversational Entity) is a computer program or an artificial intelligence which conducts a conversation via auditory or textual methods. Such programs are often designed to convincingly simulate how a human would behave as a conversational partner, thereby passing the Turing test. Chatbots are typically used in dialog systems for various practical purposes including customer service or information acquisition. Some chatterbots use sophisticated natural language processing systems, but many simpler systems scan for keywords within the input, then pull a reply with the most matching keywords, or the most similar wording pattern, from a database.</p>

<p align="justify" style="padding-left: 1em">The term “ChatterBot” was originally coined by Michael Mauldin (creator of the first Verbot, Julia) in 1994 to describe these conversational programs. Today, most chatbots are either accessed via virtual assistants such as Google Assistant and Amazon Alexa, via messaging apps such as Facebook Messenger or WeChat, or via individual organizations’ apps and websites. Chatbots can be classified into usage categories such as conversational commerce (e-commerce via chat), analytics, communication, customer support, design, developer tools, education, entertainment, finance, food, games, health, HR, marketing, news, personal, productivity, shopping, social, sports, travel and utilities.</p>

<h2>How to create chatbot?</h2>

<figure>
  <img src="/images/projects/chatbot.png" alt="chatbot.png" style="width:100%">
  <figcaption style="text-align: center; padding-left:45%;">C# Chatbot</figcaption>
</figure> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/_CSvzXmb7BI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<pre align="justify" style="padding-left: 1em">
In above video I’d to use my Persian accent! 😃
Interesting bot, but you need to add more codes as you wish to make it better. I’m talking with these bots when I’m alone. Hope you enjoy!
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Speech.Recognition;//1//adding speech recognition
using System.Speech.Synthesis;//16//adding speech synthesis
using System.IO;//23//workig with files
using AIMLbot;//51//
//22//saving sentence|action text file to debug folder
namespace AI2
{
    public partial class Form1 : Form
    { 
        private SpeechRecognitionEngine engine;//2//
        private SpeechSynthesizer speaker;//17//speech synthesis
        private Bot bot;//52//
        private User user;//52//
        private Dictionary<string, string> Commands; //24//key-value
        private Handler handler;//47//call writen class
        public Form1()
        {
            InitializeComponent();
        }
        //3//1st function
        public void LoadSpeech()
        {
            try
            {
                bot = new Bot();//53//
                bot.isAcceptingUserInput = false;//53//
                bot.loadSettings();//53//
                user = new User("Ali", bot);//53//
                bot.loadAIMLFromFiles();//53//
                bot.isAcceptingUserInput = true;//53//
                speaker = new SpeechSynthesizer();//18//create an instance
                //20//get the voices
                foreach (InstalledVoice voice in speaker.GetInstalledVoices())//20//
                {
                    this.comboBox1.Items.Add(voice.VoiceInfo.Name);
                }
                engine = new SpeechRecognitionEngine();//4//creating the instance of recognizer
                engine.SetInputToDefaultAudioDevice();//5//set the microphone
                engine.LoadGrammar(new DictationGrammar());//6//add the dictaion grammar
                engine.SpeechRecognized += new EventHandler<SpeechRecognizedEventArgs>(rec);//7//the recognition event
                engine.AudioLevelUpdated += new EventHandler<AudioLevelUpdatedEventArgs>(audioLevel);//9//
                engine.RecognizeAsync(RecognizeMode.Multiple);//11//starts the recognition
                                                              //25//
                #region Loading key-value into the dictionary
                Commands = new Dictionary<string, string>();//28//
                handler = new Handler(Commands);//48//instanciate the class
                StreamReader reader = new StreamReader("cmds.txt");//26//
                while (reader.Peek() > 0)//27//
                {
                    string line = reader.ReadLine();//27//
                    var parts = line.Split('|');//27//parts[0] key   parts[1] value
                    Commands.Add(parts[0], parts[1]);//29//the commands into the dictionary
                }
                #endregion
                //30//
                #region Create the commands Grammar
                Grammar commandsGrammar = new Grammar(new GrammarBuilder(new Choices(Commands.Keys.ToArray())));//30//
                commandsGrammar.Name = "cmds";//31//
                engine.LoadGrammar(commandsGrammar);//32//
                #endregion
            }
            catch (Exception ex) {
                MessageBox.Show(ex.Message+"\n"+ex.StackTrace);
            }
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            LoadSpeech();//12//
        }
        //8///2nd function rec
        private void rec(object s,SpeechRecognizedEventArgs e) {
            string speech = e.Result.Text;//15//
            if(e.Result.Confidence>0.2f)//after 50 0.45f changed to 0.2f
            {
                string answer = string.Empty;//46//after Handler.cs
                switch (e.Result.Grammar.Name)//33//then add new public class item called Handler.cs
                {
                    case "cmds":
                        handler.Handle(speech);//49//
                        answer = handler.Response();//50
                        break;
                    default:
                        answer = GetResponse(speech);//55//
                        break;
                }
                this.label1.Text = "You : " + speech;//15//
                speaker.SpeakAsync(answer);//19// //after 50 (speech) changed to answer
            }
        }
        //10//3rd funcion audioLevel
        private void audioLevel(object s, AudioLevelUpdatedEventArgs e)
        {
            this.progressBar1.Maximum = 100;//13//
            this.progressBar1.Value = e.AudioLevel;//14//run&see audio level//
        }

        private void comboBox1_SelectedIndexChanged(object sender, EventArgs e)
        {
            try
            {
                speaker.SelectVoice(this.comboBox1.SelectedItem.ToString());//21//
            }
            catch(Exception ex) { MessageBox.Show(ex.StackTrace); }
        }
        private string GetResponse(string input)//54//
        {
            Request request = new Request(input, user, bot);//54//
            Result result = bot.Chat(request);//54//
            return result.Output;
        }
    }
}
</pre>
    
