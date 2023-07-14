# Trabalho realizado na Semana #3

## Identification:
    CVE-2017-0144 allows remote attackers to execute arbitrary code via crafted packets.
    Affected systems include the SMBv1 server in Microsoft Windows Vista SP2; Windows Server 2008 SP2 and R2 SP1.

## Catalogation:
    CVE-2017-0144 was developed by the National Security Agency.
    It was leaked by the Shadow Brokers hacker group on april 14 2017, one month after it was patched.
    The cvvs score is 9.3, since it has complete access of the computer, but having a medium access complexity.

## Exploits:
    The EternalBlue exploits a vulnerability in Microsoft's implementation of the SMB protocol, allowing to remotely execute code on the target computer.
    SrvOs2FeaToNt exploits a vulnerability in Microsoft Windows Server 2008 R2 (x64), allowing remote execution of code.

## Attacks:
    EternalBlue has led +$1B in damages, both NotPetya and BadRabbit used it as an initial compromise vector or lateral movement.
    On 12/5/2017, WannaCry ransomware used this exploit to attack unpatched computers.
    On 27/6/2017, the exploit was again used to help carry out the 2017 NotPetya cyberattack on more unpatched computers.
    Addicionaly it was used since 1/3/2016 by Buckeye, as well as used in the Retefe banking trojan since 5/9/2017.
