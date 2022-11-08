# Linux String Substitute (sed)
```bash
ssh banner@stapp03
```
```
sudo su
```
```
cd /home
```
```bash
sed -e '/copyright/d' BSD.txt > /home/BSD_DELETE.txt
```
```
diff BSD.txt BSD_DELETE.txt 
```

*Observe that the keyword is removed*
```bash
sed -e 's/or/them/g' /home/BSD.txt > /home/BSD_REPLACE.txt
```
```bash
vi BSD_REPLACE.txt
```

*verify the output*
