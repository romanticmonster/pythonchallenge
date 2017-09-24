import urllib.request
next='http://www.pythonchallenge.com/pc/def/linkedlist.php?nothing='
ne=['5','4','8','2','7']
while ne:
    repair=next
    for i in ne:
        repair=repair+i
    ne=[]
    f=urllib.request.urlopen(repair)
    linelist=f.readlines()
    for line in linelist:
        print(line)
        for a in line:
            if chr(a)<'0' or chr(a)>'9':
                continue
            else:
                ne.append(chr(a))
        if len(ne)>5:
            ne.reverse()
            for i in range(len(ne)-5):
                ne.pop()
            ne.reverse()
        print(ne)
    
  