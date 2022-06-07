---
title: "Braille system Python"
collection: projects
type: "Undergraduate projects"
permalink: /projects/BraillesystemPython
venue: "Tabriz"
date: 2017-1-1
location: "Tabriz, Iran"
---

<h2>Braille system improvement with Python</h2>


<img src="/images/projects/LouisBraille.jpg" alt="LouisBraille.jpg" style="width:30%;margin-left:50%;">
<figcaption style="text-align: center;margin-left:57%;">Louis Braille, genius</figcaption>
 

<p align="justify" style="padding-left: 1em">Louis Braille was a French educator, catholic priest and inventor of a system of reading and writing for use by the blind or visually impaired. His system remains virtually unchanged to this day, and is known worldwide simply as braille.</p>

<h3>Braille Design, ⠃⠗⠁⠊⠇⠇⠑</h3>
<p align="justify" style="padding-left: 1em">Braille worked tirelessly on his ideas, and his system was largely completed by 1824, when he was fifteen years old. From Barbier’s night writing, he innovated by simplifying its form and maximizing its efficiency. He made uniform columns for each letter, and he reduced the twelve raised dots to six. He published his system in 1829, and by the second edition in 1837 he had discarded the dashes because they were too difficult to read. Crucially, Braille’s smaller cells were capable of being recognized as letters with a single touch of a finger.</p>

<p align="justify" style="padding-left: 1em">Braille created his own raised-dot system by using an awl, the same kind of implement which had blinded him. In the process of designing his system, he also designed an ergonomic interface for using it, based on Barbier’s own slate and stylus tools. By soldering two metal strips across the slate, he created a secure area for the stylus which would keep the lines straight and readable.</p>

<p align="justify" style="padding-left: 1em">By these modest means, Braille constructed a robust communication system.</p>

<p align="justify" style="padding-left: 1em">In his own words: “Access to communication in the widest sense is access to knowledge, and that is vitally important for us if we [the blind] are not to go on being despised or patronized by condescending sighted people. We do not need pity, nor do we need to be reminded we are vulnerable. We must be treated as equals – and communication is the way this can be brought about.”</p>

<h3>Python Code</h3>
<p align="justify" style="padding-left: 1em">I impressed by Mr Braille’s works and as social responsibility, I couldn’t ignore the opportunity to learn Braille system. To make it easier I will use python and Braille ASCII.</p>

<h4>Code 1 : python Translator</h4>
<p align="justify" style="padding-left: 1em">In simplest way We will use two corresponding list and by searching characters of input string then combining them, entire statement will be translated (converted or encode/decoded).</p>
<pre align="justify" style="padding-left: 1em">
braille = ['⠴','⠂','⠆','⠒','⠲','⠢','⠖','⠶','⠦','⠔',
			'⠁','⠃','⠉','⠙','⠑','⠋','⠛','⠓','⠊','⠚',
			'⠅','⠇','⠍','⠝','⠕','⠏','⠟','⠗','⠎','⠞',
			'⠥','⠧','⠺','⠭','⠽','⠵',
			'⠱','⠰','⠣','⠿','⠀','⠮','⠐','⠼','⠫','⠩',
			'⠯','⠄','⠷','⠾','⠡','⠬','⠠','⠤','⠨','⠌',
			'⠜','⠹','⠈','⠪','⠳','⠻','⠘','⠸']
English = ['0','1','2','3','4','5','6','7','8','9',
			'a','b','c','d','e','f','g','h','i','j',
			'k','l','m','n','o','p','q','r','s','t',
			'u','v','w','x','y','z',
			':',';','<','=',' ','!','"','#','$','%',
			'&','','(',')','*','+',',','-','.','/',
			'>','?','@','[','\\',']','^','_']
def Braille2English(BrailleText) :
	return ''.join([English[braille.index(fi)] for ch in BrailleText for fi in braille if ch == fi])
def English2Braiile(EnglishText) :
	return ''.join([braille[English.index(fi)] for ch in EnglishText for fi in English if ch == fi])
</pre>
<p align="justify" style="padding-left: 1em">I’d tried the code in Jupyter Notebook and got the results as :  <br>
In [2] : English2Braiile(‘hi, i am ali bakhshi.’)  <br>
Out[2]: ‘⠓⠊⠠⠀⠊⠀⠁⠍⠀⠁⠇⠊⠀⠃⠁⠅⠓⠎⠓⠊⠨’  <br><br>

In  [3]: Braille2English(‘⠓⠊⠠⠀⠊⠀⠁⠍⠀⠁⠇⠊⠀⠃⠁⠅⠓⠎⠓⠊⠨’)  <br>
Out[3]: ‘hi, i am ali bakhshi.’</p>

<p align="justify" style="padding-left: 1em">#future developments :  </p>
 <ol>
  <li>improvement of characters</li>
  <li>adding more languages, uni-codes</li>
  <li>GUI design (Interface)</li>
  <li>TTS (Text to speech)</li>
  <li>OCR (Optical character recognition)</li>
  <li>STT (Speech to text)</li>
  <li>Machine Learning algorithms (Better Predictions)</li>
</ol>
