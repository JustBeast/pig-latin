pig-latin
=========
import os
def pigw(word):
	if word[0] == "a" or word[0] == "e" or word[0] == "i" or word[0] == "o" or word[0] == "u":
		return word + "yay"  
	else: return word[1: ] + word[0] + "ay"

def pigs(sentence):
	piggy=[]
	for x in sentence.split():
		piggy.append(pigw(x))
	return " ".join(piggy)



def pig(text):
	piggy = []
	for x in text.split("."):
		if x != "":
			piggy.append(pigs(x.strip()))
	return ".  ".join(piggy)





s = raw_input("Enter a sentence: ")
print pig(s)

os.system("say " + pig(s))

