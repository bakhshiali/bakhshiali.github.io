---
title: "Braille system Python"
collection: projects
type: "Undergraduate projects"
permalink: /projects/BraillesystemPython
venue: "Tabriz"
date: 2017-1-1
location: "Tabriz, Iran"
---

Braille system Python

<b>Louis Braille, genius</b>

![LouisBraille.jpg](/images/projects/LouisBraille.jpg)

Louis Braille was a French educator, catholic priest and inventor of a system of reading and writing for use by the blind or visually impaired. His system remains virtually unchanged to this day, and is known worldwide simply as braille.

<b>Braille Design, ⠃⠗⠁⠊⠇⠇⠑</b>  
Braille worked tirelessly on his ideas, and his system was largely completed by 1824, when he was fifteen years old. From Barbier’s night writing, he innovated by simplifying its form and maximizing its efficiency. He made uniform columns for each letter, and he reduced the twelve raised dots to six. He published his system in 1829, and by the second edition in 1837 he had discarded the dashes because they were too difficult to read. Crucially, Braille’s smaller cells were capable of being recognized as letters with a single touch of a finger.

Braille created his own raised-dot system by using an awl, the same kind of implement which had blinded him. In the process of designing his system, he also designed an ergonomic interface for using it, based on Barbier’s own slate and stylus tools. By soldering two metal strips across the slate, he created a secure area for the stylus which would keep the lines straight and readable.

By these modest means, Braille constructed a robust communication system.

In his own words: “Access to communication in the widest sense is access to knowledge, and that is vitally important for us if we [the blind] are not to go on being despised or patronized by condescending sighted people. We do not need pity, nor do we need to be reminded we are vulnerable. We must be treated as equals – and communication is the way this can be brought about.”

Python Code
I impressed by Mr Braille’s works and as social responsibility, I couldn’t ignore the opportunity to learn Braille system. To make it easier I will use python and Braille ASCII.

Code 1 : python Translator
In simplest way We will use two corresponding list and by searching characters of input string then combining them, entire statement will be translated (converted or encode/decoded).
<pre>
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
I’d tried the code in Jupyter Notebook and got the results as :  
In [2] : English2Braiile(‘hi, i am ali bakhshi.’)  
Out[2]: ‘⠓⠊⠠⠀⠊⠀⠁⠍⠀⠁⠇⠊⠀⠃⠁⠅⠓⠎⠓⠊⠨’  

In  [3]: Braille2English(‘⠓⠊⠠⠀⠊⠀⠁⠍⠀⠁⠇⠊⠀⠃⠁⠅⠓⠎⠓⠊⠨’)  
Out[3]: ‘hi, i am ali bakhshi.’

#future developments :  
1) improvement of characters  
2) adding more languages, uni-codes  
3) GUI design  
4) TTS (Text to speech)  
5) OCR (Optical character recognition)  
6) STT (Speech to text)  
7) Machine Learning algorithms (Better Predictions)  

