## What is Network
- 노드들이 자원을 공유할 수 있게 하는 디지털 전기통신망.
- 그 규모에 따라 구분할 수 있다.
  - PAN (Personal)
  - LAN (Local)
  - MAN (Metropolitan)
  - WAN (Wide)


## What is an IP address
### IPv4
- 32비트 주소체계
- 8비트씩 끊어서 '.'을 기준으로 10진수로 표현
- `127.` 으로 시작하는 모든 IPv4주소는 특별한 용도를 위해 예약됨.
  - ex) 127.0.0.1 (localhost)
### IPv6
- IPv4로는 모든 단말에 주소를 부여하기 부족해져 128비트로 길이를 늘림.
- 16진수 4개를 묶어 8개를 쓰고 ':' 로 구분 (4 * 4 * 8 = 128)
### IP Address Class
- ip address는 클래스라는 개념이 존재한다.


## What is a Netmask
- 네트워크 주소 부분의 비트를 1로 치환한 것.
- IP주소와 넷마스크를 AND연산 시 네트워크 주소를 얻는다.
### Network Address
- 해당 네트워크의 첫번째 IP주소


## What is the subnet of an IP with Netmask
- 서브넷은 부분망이라는 뜻으로 IP를 사용하는 장치 수에 따라 효율적으로 사용할 수 있도록 고안됐다.
- 서브넷 마스크를 사용해 여러개의 서브넷 네트워크로 분할 하는 것을 subnetting이라고 한다.


## What is the broadcast address of a subnet
### Broadcast Address
- 네트워크에 있는 클라이언트 모두에게 데이터를 보낼 때 사용.
- 브로드캐스트 주소는 해당 서브넷의 마지막 주소로 볼 수 있다.
- 네트워크 주소에서 서브넷 마스크의 0부분의 값을 모두 1로 바꾸면 얻을 수 있다.

## What are the differences between public and private IPs
### public IP
- 공인 IP는 전세계에서 유일한 IP주소를 갖는다.
- 외부에 공개되어 있기 때문에 인터넷상의 다른 pc에서 접근이 가능하다.
- ISP에 의해 할당한다.

### private IP
- 사설 IP는 특정 집단 내부에서 사용할 목적의 주소.
- IPv4의 주소 부족으로 서브넷팅된 IP로 라우터에 의해 할당됨.
- 주소 대역
  - Class A : 10.0.0.0 ~ 10.255.255.255
  - Class B : 172.16.0.0 ~ 172.31.255.255
  - Class C : 192.168.0.0 ~ 192.168.255.255


## What is a class of IP addresses
- A Class : 0 ~ 127 (0.0.0.0 ~ 127.255.255.255)
  - 인데 0.X.X.X 와 127.X.X.X(루프백)는 제외해야 한다.
  - 첫번째 옥텟까지 네트워크주소 (서브넷 마스크가 255.0.0.0)
- B Class : 128 ~ 191 (128.0.0.0 ~ 191.255.255.255)
  - 서브넷 마스크 = 255.255.0.0
- C Class : 192 ~ 223 (192.0.0.0 ~ 223.255.255.255)
  - 서브넷 마스크 = 255.255.255.0
- D Class : 224 ~ 239 (224.0.0.0 ~ 239.255.255.255)
- E Class : 240 ~ 255 (240.0.0.0. ~ 255.255.255.255)


## What is TCP
- 연결형 서비스를 지원하는 프로토콜로 패킷을 추적하고 관리한다.
- 흐름과 혼잡을 제어하고 연결을 보장하므로 높은 신뢰성을 가지지만 UDP보다 속도가 느리다.
- 가상 회선 방식을 사용, 3-way handshaking 통해 연결 설정, 4-way handshaking 통해 해제


## What is UDP
- 비연결형 서비스로 데이터그램 단위로 처리한다.
- 정보를 보내거나 받는다는 신호를 처리하지 않으며 최소한의 오류만 검출하므로 신뢰성이 낮은 대신 TCP보다 속도가 빠르다.
- 스트리밍같이 신뢰성보다 연속성이 중요한 서비스에서 사용됨.


## What are the network layers
- 네트워크 통신이 일어나는 과정을 계층화 한것.
- 계층화를 통해 특정한 계층에 문제가 생기면 유지보수가 용이하다.
- 또 각각의 계층이 표준화되어 효율성을 높일 수 있다.


## What is the OSI model
- OSI(Open Systems Interconnection Reference Model)는 국제표준화기구에서 개발한 모델로, 컴퓨터 네트워크 프로토콜 디자인과 통신을 계층으로 나누어 설명한 것이다.
- 각 계층은 상, 하위 계층과 정보를 주고 받아 역할을 수행한다.


## What is a DHCP server and the DHCP protocol
- 단말에게 IP address를 일정 시간동안 lease, 할당해주는 프로토콜.
- DHCP서버는 클라이언트에게 IP address를 할당해준다.


## What is a DNS server and the DNS protocol
- 도메인 네임과 IP address의 대응 관계를 데이터베이스로 구축해 사용하는 인터넷 프로토콜.
- DNS를 운영하는 서버를 name server라고 한다.


## What are the rules to make 2 devices communicate using IP addresses
## How does routing work with IP
## What is a default gateway for routing
## What is a port from an IP point of view and what is it used for when connecting to another device
