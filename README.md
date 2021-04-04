# -#!/usr/bin/env python
# coding: utf-8

# In[6]:


from random import shuffle
from random import randint
suit = ["♠", "♥", "♦", "♣"]
order=['A','2','3','4','5','6','7','8','9','10','J','Q','K']
pokers=[]
hand1=''
hand2=''
hand11=''
hand22=''
hand1final=''
hand2final=''
pokerscopy=[]
count1=[0]*52
count2=[0]*52
iin1=[0]*13
iin2=[0]*13
h3=[]
rounds=1
thing1=0
thing2=0
fxxk=0
z=0
w=0
k=0
c=0
b=[]
h6=[]
ww=0
h1=[]
h2=[]
for i in suit:
    for j in order:
        pokers.append(i+' '+j)
shuffle(pokers)
for h in range(0,52):
        poker_copy=pokers
        b.append(poker_copy[h].replace(' ',''))    
n=randint(1,2)
for i in range(0,26):
    hand1+=pokers[i]
    hand11+=b[i]
    if i !=25:
        hand1+=' '
        hand11+=','
for j in range(26,52):
    hand2+=pokers[j]
    hand22+=b[j]
    if j !=51:
        hand2+=' '
        hand22+=','
if n%2==0:
    hand11+=',👻'
else:
    hand22+=',👻'
hand1test=hand1.split(' ')
hand2test=hand2.split(' ')
for i in range(1,53,2):
    if hand1test[i]=='A':
        thing1=1
    if hand1test[i]=='2':
        thing1=22
    if hand1test[i]=='3':
        thing1=3
    if hand1test[i]=='4':
        thing1=4
    if hand1test[i]=='5':
        thing1=5
    if hand1test[i]=='6':
        thing1=6
    if hand1test[i]=='7':
        thing1=7
    if hand1test[i]=='8':
        thing1=8
    if hand1test[i]=='9':
        thing1=9
    if hand1test[i]=='10':
        thing1=10
    if hand1test[i]=='J':
        thing1=11
    if hand1test[i]=='Q':
        thing1=12
    if hand1test[i]=='K':
        thing1=13
    for j in range(1,53,2):
            if i==j:
                continue
            if hand1test[i]!=hand1test[j]:
                if count1[i-1]==0:
                    count1[i-1]+=thing1
            if hand1test[i]==hand1test[j]:
                count1[i]+=1
                if count1[i-1]==0:
                    count1[i-1]+=thing1
for i in range(0,52):
    if count1[i]==0:
        h1.append(hand1test[i-1])
        h1.append(hand1test[i])
        hand1final+=hand1test[i-1]
        hand1final+=hand1test[i]
        hand1final+='零'
    if count1[i]==2 and count1[i-1]==1:
        iin1[0]=i
    if count1[i]==2 and count1[i-1]==22:
        iin1[1]=i
    if count1[i]==2 and count1[i-1]==3:
        iin1[2]=i
    if count1[i]==2 and count1[i-1]==4:
        iin1[3]=i
    if count1[i]==2 and count1[i-1]==5:
        iin1[4]=i
    if count1[i]==2 and count1[i-1]==6:
        iin1[5]=i
    if count1[i]==2 and count1[i-1]==7:
        iin1[6]=i
    if count1[i]==2 and count1[i-1]==8:
        iin1[7]=i
    if count1[i]==2 and count1[i-1]==9:
        iin1[8]=i
    if count1[i]==2 and count1[i-1]==10:
        iin1[9]=i
    if count1[i]==2 and count1[i-1]==11:
        iin1[10]=i
    if count1[i]==2 and count1[i-1]==12:
        iin1[11]=i
    if count1[i]==2 and count1[i-1]==13:
        iin1[12]=i
for i in range(0,13):
    if iin1[i]!=0:
        h1.append(hand1test[iin1[i]-1])
        h1.append(hand1test[iin1[i]])
        hand1final+=hand1test[iin1[i]-1]
        hand1final+=hand1test[iin1[i]]
        hand1final+='零'
hand1finals=hand1final[:-1]
hand1finalss=hand1finals.replace('零',',')

for i in range(1,53,2):
    if hand2test[i]=='A':
        thing2=1
    if hand2test[i]=='2':
        thing2=22
    if hand2test[i]=='3':
        thing2=3
    if hand2test[i]=='4':
        thing2=4
    if hand2test[i]=='5':
        thing2=5
    if hand2test[i]=='6':
        thing2=6
    if hand2test[i]=='7':
        thing2=7
    if hand2test[i]=='8':
        thing2=8
    if hand2test[i]=='9':
        thing2=9
    if hand2test[i]=='10':
        thing2=10
    if hand2test[i]=='J':
        thing2=11
    if hand2test[i]=='Q':
        thing2=12
    if hand2test[i]=='K':
        thing2=13
    for j in range(1,53,2):
            if i==j:
                continue
            if hand2test[i]!=hand2test[j]:
                if count2[i-1]==0:
                    count2[i-1]+=thing2
            if hand2test[i]==hand2test[j]:
                count2[i]+=1
                if count2[i-1]==0:
                    count2[i-1]+=thing2
for i in range(0,52):
    if count2[i]==0:
        h2.append(hand2test[i-1])
        h2.append(hand2test[i])
        hand2final+=hand2test[i-1]
        hand2final+=hand2test[i]
        hand2final+='零'
    if count2[i]==2 and count2[i-1]==1:
        iin2[0]=i
    if count2[i]==2 and count2[i-1]==22:
        iin2[1]=i
    if count2[i]==2 and count2[i-1]==3:
        iin2[2]=i
    if count2[i]==2 and count2[i-1]==4:
        iin2[3]=i
    if count2[i]==2 and count2[i-1]==5:
        iin2[4]=i
    if count2[i]==2 and count2[i-1]==6:
        iin2[5]=i
    if count2[i]==2 and count2[i-1]==7:
        iin2[6]=i
    if count2[i]==2 and count2[i-1]==8:
        iin2[7]=i
    if count2[i]==2 and count2[i-1]==9:
        iin2[8]=i
    if count2[i]==2 and count2[i-1]==10:
        iin2[9]=i
    if count2[i]==2 and count2[i-1]==11:
        iin2[10]=i
    if count2[i]==2 and count2[i-1]==12:
        iin2[11]=i
    if count2[i]==2 and count2[i-1]==13:
        iin2[12]=i
for i in range(0,13):
    if iin2[i]!=0:
        h2.append(hand2test[iin2[i]-1])
        h2.append(hand2test[iin2[i]])
        hand2final+=hand2test[iin2[i]-1]
        hand2final+=hand2test[iin2[i]]
        hand2final+='零'
hand2finals=hand2final[:-1]
hand2finalss=hand2finals.replace('零',',')
if n%2==0:
    hand1finalss+=',👻'
    h1.append('👻')
    h1.append(' ')
    
else:
    hand2finalss+=',👻'
    h2.append('👻')
    h2.append(' ')
    
 

h1final=''
h2final=''



          
print('Initial')
print('player1\'s hand:%s'%hand11)
print('player2\'s hand:%s'%hand22)
print('')
print('Game start...') 
print('player1\'s hand:%s'%hand1finalss)
print('player2\'s hand:%s'%hand2finalss)
print('')


def xplan(h1,h2):
    rounds=1
    h1final=''
    h2final=''
    len1=len(h1)
    n1=randint(0,(len1/2)-1)
    h2.append(h1[2*n1])
    h2.append(h1[2*n1+1])
    len2=len(h2)
    if h1[2*n1]!='👻':
        for i in range(len2-2):
            if h2[-1]==h2[i]:
                count3=i
        del h2[count3]
        del h2[count3-1]
        del h2[-1]
        del h2[-1]
    h1[2*n1+1]=h1[2*n1+1].replace(' ','')
    print('%s%s is deawn.'%(h1[2*n1],h1[2*n1+1]))
    del h1[2*n1]
    del h1[2*n1]
    for i in range(len(h1)):
        h1final+=h1[i]
        if i%2==1:
            h1final+=','
    h1final1=h1final[:-1]
    h1final11=h1final1.replace(' ','')
    for i in range(len(h2)):
        h2final+=h2[i]
        if i%2==1:
            h2final+=','
    h2final2=h2final[:-1]
    h2final22=h2final2.replace(' ','')
    
    rounds+=1
    return [h1final11,h2final22]

while len(h1)!=2 or len(h2)!=2:
    print('Turn:%d'%rounds)
    [h1final11,h2final22]=xplan(h1,h2)
    print('player1\'s hand:%s'%h1final11)
    print('player2\'s hand:%s'%h2final22)
    rounds+=1
    if h1==[]:
        break
    if h2==[]:
        break
    print('Turn:%d'%rounds)
    [h1final11,h2final22]=xplan(h2,h1)
    print('player1\'s hand:%s'%h2final22)
    print('player2\'s hand:%s'%h1final11)
    rounds+=1
    if h1==[]:
        break
    if h2==[]:
        break
print('')
if h1==[]:
    print('player2 lose.')
if h2==[]:
    print('player1 lose.')






