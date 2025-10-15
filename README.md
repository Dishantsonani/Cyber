1.Steghide :
cd Downloads,
cat > Demo.txt,
steghide embed -cf images.jpeg -ef Demo.txt -sf images.jpeg,
steghide extract -sf images.jpeg

2.Encryption-Decryption :
openssl enc -aes-256-cbc -salt -in Demo.txt -out Demo.enc,
openssl enc -aes-256-cbc -d -in Demo.enc -out Decrypted.txt,
cat Demo.enc,
cat Decrypted.txt

3.Hashing using openssl :
openssl dgst -sha256 Demo.txt,
sha256sum Demo.txt,
sha256sum Demo.txt > hash.txt,
sha256sum -c hash.txt

4.John the ripper :
echo b24331b1a138cde62aa1f679164fc62f > hashpsw.txt,
cat hashpsw.txt,
john hashpsw.txt --format=Raw-MD5,
create zip file on desktop and use password 12345 and my filename is hashpsw.zip,
cd Desktop,
ls,
zip2john hashpsw.zip > hash.txt
