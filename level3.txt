def cap(c):
    if ord(j)<ord('A') or ord(j)>ord('Z'):
        a=0
    else:
        a=1
    return a
def min(c):
    if ord(j)<ord('a') or ord(j)>ord('z'):
        a=0
    else:
        a=1
    return a
a=open('D:/ma.log')
list=a.readlines()
capa=0
an=0
minu=0
for i in list:
    for j in i:
        if capa>3:
            if cap(j)==1:
                pass
            else:
                capa=0
                minu=0
                an=0
        elif capa==3 and minu==1 and an==3:
            if min(j)==1:
                print(get)
            else:
                capa=4
                minu=0
                an=0
        elif capa==3 and minu==1 and an<3:
            if cap(j)==1:
                an+=1
            else:
                capa=0
                minu=0
                an=0
        elif capa==3 and minu<1:
            if min(j)==1:
                minu=1
                get=j
            else:
                capa=4
                minu=0
                an=0
        else:
            if min(j)==1:
                capa=0
            else:
                capa+=cap(j)
        