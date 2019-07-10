 00:00:02
Hello. Welcome to see us 6823 or security. This is week number three farmers for our summer 2019 session. Today is Monday, June 17 2009
00:00:18
Today we will be continuing our lecture to network reconnaissance and move on to lecture three which is that work exploitation.
00:00:29
So we've been following the network attack methodology which is a five step process that we generally talk about in this class. So the network attack by far G is
00:00:42
Reconnaissance
00:00:45
Performed scanning
00:00:48
The five when abilities.
00:00:51
Exploit and then post exploitation. So we kind of like what duty steps already some of them right so reconnaissance is finding information about our network. And that's, that is what we've been talking about last week and we'll talk about this week as well.
00:01:07
Then we'll talk about scanning that is defined a host in the network. Right, right, to find the IP addresses to find what systems are running and such.
00:01:20
Then we move on to one ability intensification that is finding one one or both services ports applications architecture issues password reuse issues physical security issues, trying to find one abilities that can be exploited.
00:01:38
Then we do exploitation, you found that one abilities. Now you can exploit it. And then after exploitation, you have access to a network.
00:01:49
So after you have access to that or you perform post exploitation, which is what do you do after you have access to network. Now that you have access to networking. What do you do alright you hacked into target. Now what do you do, you would sell to malware to
00:02:08
Gather credit card information from the point of sale systems.
00:02:12
You can delete logs you can maintain access, like, make sure that after the system reboots you're still able to get back onto the system so you can continue working on it next week right that's post exploitation right and that's that's a big part of it too, but
00:02:30
This whole process from beginning to end, takes a long, long time. Like sometimes you see in the movies. It takes maybe like five seconds for them to like
00:02:39
recon and that org do the scanning exploited it and get into it. Well, it just really doesn't work like that. It takes months, months, months, and years to do this for example.
00:02:52
Sony. Sony Pictures, they're the ones that got hacked by North Korea. North Korea within the networks for nine months. So this whole step between reconnaissance
00:03:04
All the way to exploitation and post exploitation, the whole process took nine months for them to do.
00:03:11
Essentially North Korea went into Sony Pictures networks and just stayed there and continue to work and try to find one abilities and try to map out the network.
00:03:21
And all the way to the release that silly movie about North Korea. Oh, what's the name of it before they decide to do something about it. So there were there for nine months.
00:03:34
And yes, the interview the emergency that I started for the sole purpose.
00:03:40
That it costs the North Korea to attack Sony Pictures and it was was okay.
00:03:49
So typically, this process takes a long time. Target. Target lost over 100 million credit card numbers. A couple of years ago right to target attack is one of the one of your reading materials.
00:04:01
And the attackers were in the network for how long it was about a month right a month to six weeks to go through the whole process before they
00:04:10
Are able to start stealing credit card numbers from Target, it takes a long time. So yesterday and a little bit today what we're going to talk about reconnaissance right the steps that you take in order to
00:04:25
Case the joint.
00:04:27
And we'll move on to scanning, which is finding the IPS finding that work, finding it finding the host and then define when abilities exploit when abilities and then post exploitation, what do you do afterwards to the laws and so on.
00:04:44
Besides the MO one. So as a reminder, every week for 10 weeks we're going to have a number of exercises and if you decide to do all the exercises.
00:04:55
You will get a bonus on top of your grade equivalent to one homework assignment and that two to 2.5% depending on the assignments that we give and that's
00:05:06
Almost love to pump you up the next grade. So let's say you have an A minus, but really, really close today doing this one assignments will bump you up to the point to a for a
00:05:18
So exercise. Number one, what are the six steps of the network or Carson's by RG that we use in this class. So we talked about this difficulty last week. What a six steps of network Constance if RG since you should be familiar. Let's take one minute to do this.
00:06:01
10 seconds.
00:06:39
Alright.
00:06:41
So,
00:06:43
The six steps of the network reconnaissance mythology that we use in this class is collect Public Information Network discovery host Discovery Service discovery analyze that data.
00:06:58
And recursion. So
00:07:02
Don't be confused between the network attack mythology, which is the overall process of identifying the host to attack and how to attack it.
00:07:12
And the network recall since with RG which is just a subset of the network attack mythology. Now, these two are just mythologies, and I i want really want to say that this is just the way that we we use it in this class.
00:07:28
And when you go to, you know, when you become a cyber security professional and you follow the mythology at your workplace or or or as a team, or as a blue team.
00:07:40
It will be slightly different. But the idea is exactly the same no matter what, no matter what you call these and no matter how you group them.
00:07:49
These are the steps that you must do in order to perform and network attack and same thing for reconnaissance. No matter what you call these different sections, no matter what, what, you know how you group them into each other.
00:08:06
All the steps are sort of thing, right, no matter what the process for performance network record sentence is kind of public information.
00:08:18
Gather information from additional sources right as much in network information. She can analyze information forgot my stuff and do again and again and again to get more information. So you can start attacking them right no matter what the mythology. Is this the same
00:08:40
But before we continue to lecture last piece muddled points. I had a number of people who had some issues with brute force for DNS and split DNS. So I'm just go over this topic again.
00:08:55
So,
00:08:56
DNS.
00:08:58
DNS is the process that helps your web browser. Find the IP address associated with a domain name. So let's say you're trying to go to nyu.edu and you type in mit.edu into your web browser, your web browser will doesn't know what IP address. So by browser will make a DNS request for nyu.edu
00:09:22
And then the DNS server will reply with the IP address and then you can just go to the IP address associated with mit.edu
00:09:34
Now the thing is there's also a number of subdomains as well. So you have like www.nyc.edu new classes@nyu.edu
00:09:47
What else is there home that nyu.edu engineering the NYU the EDU like what else is there right there's Albert's at nyu.edu
00:10:00
Does anyone know and the others.
00:10:04
Right, Albert, those, those are the main ones I use probably every school has one, I think as well.
00:10:15
But the main point is there are a lot of domain that there's laws subdomains associated with nyu.edu
00:10:23
And sometimes there might be ones out there that you don't even know. Like, for example, you could have FTP that nyu.edu but I don't know if they exist right I can try. So I can check if I want to know if FTP to NYU to edu exist. I can just do it and the stock up
00:10:44
On it, or I can just go to a web browser and find out whether
00:10:49
FTP and while you're at you exist or not exist. So actually let me try that we try that. Right now I see no reason not to do that.
00:11:00
Actually sharing is tough. Let me try to share it here, why you should. Okay, there we go. So you should see my Google Chrome right now so DNS lookup.
00:11:15
And which one do we use last time. This one seems to work very well. So does FTP nyu.edu doesn't exist.
00:11:26
It does not exist any others. How about
00:11:31
About
00:11:33
Test test@nyu.edu, it does not exist. You don't know any weird one sex they exist on try Albert
00:11:43
Over to MIT edu. Yep. He says to his IP address.
00:11:49
About some weird ones like
00:11:52
How about www to
00:11:55
It that does not exist.
00:11:57
So,
00:12:00
What I'm trying to do here. Oh, man. Yeah, yeah, man. How interesting. So BED BED that nyu.edu directors. How about that they have like bed to know how about math test thanks is no it doesn't exist.
00:12:19
So what I'm doing is I'm, I'm just trying different one to see if I can find one that works or not. Sometimes I have that btw too.
00:12:33
So I'm just trying to find
00:12:37
Something subdomains associated with it.
00:12:40
Just doing a just trying different ones and trying different ones over and over again. And by doing this. It's called brute force forward DNS lookup, and they're incorrect my PowerPoint slide.
00:12:55
Here we are.
00:12:58
So I am performing a brute force forward DNS lookup. That is, I am trying to try to hundreds and thousands of combinations from a Word file and it's
00:13:09
Generally just really easy to I just get a Word file of, you know, common names as go and just keep trying and trying and trying to find one and a purpose of this is just
00:13:21
I want to find something that may be, it was Miss configured, baby. It was a test server, maybe something that they forgot about. And this happens.
00:13:30
Like for any of you who worked in a large enterprise organization, you know, that happens computers go online people forget about it. Five years later.
00:13:39
You know, you suddenly realize, oh wait, we have this Windows XP machines don't want to network and we didn't even realize this happens all the time, right. So brute force for DNS is a way to just keep trying different names, you can try random numbers you can try common
00:13:57
host names and try all these things.
00:14:01
And what can you do to stop it right, just stop it. We use split DNS and we use the DNS because
00:14:09
There are legitimate reasons that you need to have your test server. So if you want to, like, you know, make a new homepage.
00:14:17
You have to have some server to test it out so you can do like www test that mit.edu so you can go and try out test it out. Make sure everything works perfectly and such.
00:14:29
But in order to do that.
00:14:32
You also don't want people from outside the internet being able to access it. So you let's say your web developer or maybe like your database developer and you made a new database server and you just want to test it out.
00:14:46
You don't want people have that outside being able to get the IP address. So you do split DNS split DNS is when you have two different servers.
00:14:58
So you have an internal DNS server for internal folks and external DNS server for external folks and people from internal
00:15:07
You can do whatever you want. For example, you can do like your host name at that domain. For example, if you have windows so you can like send
00:15:16
Messages to local computers and have them be able to be found the Ns or you can do your diet www test that MIT edu so we can fully test it out or your database server.
00:15:29
fully tested out internally before you put into production and you put that in your internal DNS your external DNS, you just use just for your externally facing stuff and nothing else. Right. So that's the DNS and brute force for it attacks.
00:15:49
Some other questions.
00:15:55
I think I covered the major ones.
00:16:02
The main topic for today is port scanning
00:16:06
And port scanning is a process that you use to identify the ports on a particular host. So as you know,
00:16:15
Every host on internet or every host has, you know, if they talk on TCP IP.
00:16:22
They have, you know, port numbers so you know you have some ports for TCP and you have ports for UDP and there are quite a, quite a number of ports right there are two racer 32 points for TCP and to racer dirty to port for UDP. There are a lot of ports.
00:16:45
Right 64,000 ports 65,000 ports for TCP and $65 for UDP.
00:16:52
And specifically for TCP in order to start a connection, you have to perform a TCP three way handshake and look into how that works.
00:17:07
Well, that means me share a different screen.
00:17:10
Or. Here we go.
00:17:18
See, I always have to make sure that I'm sharing the right screen, right, the right screen on one moment, the middle
00:17:32
So you should be able to see a slide SF TCP three way handshake.
00:17:38
Okay, great. Thank you.
Unknown Speaker
00:17:41
All right, great.
Phillip Mak
00:17:43
Thank you.
00:17:45
What's everyone's favorite website. Here we have a favorite website Amazon.
00:17:57
Will be using this at NYU. So let's use a and why you. Okay, so when you perform a TCP three way handshake.
00:18:08
When you want to go to NYU, go to NYU and a website, the first thing you do is you have to establish a TCP connection. If you want to talk on a protocol that uses TCP, the first thing you do is a TCP three way handshake and it generally works like this. You send a TCP
00:18:30
TCP syn packet
00:18:35
Right. The first step.
00:18:38
So you Ellis and say TCP syn packet to NYU.
00:18:43
And you will return with a TCP sync.
00:18:57
And then
00:18:59
Alice with Sunday TCP SYN ACK, ACK or does TCP
00:19:06
Know, sometimes recorded TCP sing.
00:19:10
Back right
00:19:15
Which is basically the act of the scene, but basically as a TCP act.
00:19:23
So this is a TCP three way handshake. Every time there's a
00:19:29
There's a TCP connection, you start with a TCP three way handshake and after the TCP three way handshake, then you start to have bi directional communications so afterwards.
00:19:42
You start sending in other information as well.
00:19:48
So for example, if you're trying to make a you know a connection to a website. The next thing you do is the HTTP request.
00:20:01
Right so TCP
00:20:04
TCP sync TCP
00:20:07
TCP and then
00:20:10
Your higher order level request. So if you have a HTTP request, you go directly to the HTTP request. So this is something like
00:20:22
It or something, this will be something that looks like get in the HTML or something like that, right, something along that lines.
00:20:34
And, you know, regular HTTP request is just pure plain text. It is literally sending those characters over the TCP connection.
00:20:45
Or if you're trying to establish a te LL s connection first SSL to s connection first, then you send a to a TMS. Hello.
00:21:02
Message first and this is to establish a to secure connection before you do your HTTP connection and so on. So, this is the TCP three way handshake.
00:21:15
But actually there's there's more to this which which I kind of omitted, a little bit.
00:21:26
So this TCP syn packet. It has some information in it, so it has a source port number for
00:21:39
Right. And it has a destination port number. Would anyone know
00:21:47
If I'm trying to connect to HTTP. What is a source and destination port for this for this packet
00:21:57
And this is not a bonus question. It's just, I'm just asking talking out loud here.
00:22:05
Right so point at that point at that shorts with this nation ports.
00:22:14
Right. How about what's the source port.
00:22:22
Right, it's something greater than one or two for
00:22:26
One or two, three.
00:22:28
So source so destination point is at
00:22:32
An ad means HTTP.
00:22:35
In a source port is something greater.
00:22:38
Greater than one or two, three.
00:22:41
Right, that's the default, it could be anything but by default, your web browser will be picking some random number something above one or two, three up the second packet the TCP SYN ACK, what is the source and destination port here.
00:22:56
And then I'm going to ask for this one for the third one.
00:23:14
So you Allison connection to NYU source port is is x is greater one or two, three dozen he points at every turn to use the same ports. So source port is at
00:23:27
And destination point is whatever X was, that was great and one or two right whatever was just uses the same place. It's the same ports.
00:23:38
And then the TCP
00:23:41
So source port.
00:23:43
What's this a social support and destination point here.
00:23:51
Yeah, yeah, it's x greater than one or two, three and the destination port.
00:24:00
Yeah, it's 82
00:24:06
So this is a TCP three way handshake.
00:24:11
Right. And actually, this is when the ports open so
00:24:16
Port
00:24:19
Is open
00:24:29
Question is does, doesn't the server assign a port grade and one or two, three for the stock a separate from a server socket. I'm in general.
00:24:41
In general, Windows and Linux follows nearly the same nearly the same thing.
00:24:52
The port that you're trying to reach, which is basically what we normally called a port number like point at Port 2122 port 53 whatever does destination port. And that's always the same. So this web server on NYU.
00:25:08
Web server. It's handling thousands and thousands and thousands of
00:25:13
At the same time, but the source port is basically some randomly generated number. And usually, usually it's greater than one or two, three, right, it could be different. I think
00:25:29
It's not actually going in order to agree it's at something like 10,000 or above or something. At least that's what Windows users right window, you just pick the number above 10,000 as such but from a
00:25:42
From a protocol level, the number has to be greater than one or two, three, because anything under is reserved
Unknown Speaker
00:25:53
Oh,
Phillip Mak
00:25:55
Let me know if I did not answer your question.
00:25:59
So this is a TCP three way handshake and this is what happens when the port is open, right. So when the port is open.
00:26:07
This is what it looks like now.
00:26:11
What is the ports closed.
00:26:15
Right. What is the point is closed. What's
00:26:18
How is it gonna look like.
00:26:21
Let me make a copy of the slide here.
00:26:26
So what if
00:26:30
What if the point is closed.
00:26:33
Well, what happened here. So let me delete this and let me click on this. Yeah.
00:26:41
Alright so Alice is trying to connect to NYU.
00:26:45
And Alice makes a connection to NYU.
00:26:49
source port x is greater wanted to do a
00:26:53
destination point is at
00:26:56
The port is close right NYU does not have a web server or the web server is not functioning or it's, you know, there's a firewall away or whatever. What is going to happen here.
00:27:12
What's going to happen here.
00:27:14
Right. That's right. So TCP
00:27:19
Reset set
00:27:26
The source port and destination port is why it's exactly the same.
00:27:44
So the support at nation point is whatever x plus
Unknown Speaker
00:27:56
And that's it.
Phillip Mak
00:28:00
Right, so we have the two major cases. Right. The first one is put is open.
00:28:08
And the second one is port is closed.
00:28:14
We have another option.
00:28:17
We have another option.
00:28:23
The third thing that can happen when you send a TCP syn packet is you can get an ICMP unreachable. Right. So the third way.
00:28:34
Third Way.
00:28:38
You send a TCP syn packet, you get a ICMP on reachable
00:28:55
Allison's a message to NYU and my you response with ICMP unreachable.
00:29:01
And what this means in this case is that in a normal host
00:29:08
A a normal Windows or Linux host. They do not send ICMP unreachable based on TCP. This usually means there's a firewall in a way that's rejecting packets. So now there's something here in between the firewall between and the firewalls gain away.
Unknown Speaker
00:29:33
Change this color to something else.
00:29:49
Change the color here.
Phillip Mak
00:29:55
Change it to like read for firewall. There it is.
00:30:03
So when the firewalls and the way if I walk in with the backpack get
00:30:19
When the firewall rejects the packet. It just nicely tells you you can't get here, right. It's a very nice way to tell you you can't reach it that ports not open. You can't get in the firewalls and
00:30:34
It's just a really, really nice way to do it. And the fourth thing that could possibly happen when you send a TCP syn packet is well this slide should be easy to write. There's nothing happens.
00:30:49
So the fourth way.
00:30:53
Nothing, no response.
00:31:04
So basically nothing returns, nothing, nothing is there at all. So let's go over the four steps again.
00:31:13
The first thing. The first way is you send a TCP syn packet and the TCP three way handshake work exactly as intended, and everything's fine. This means that the board is open.
00:31:30
Let's say you send a TCP syn packet. And the point is closed, you get a reset back right this is very clear. You get a reset. The point is closed. Well, that's, that's the only thing you can tell
00:31:46
Third thing that can happen is that something in the way something is saying you can't get here and you get an ICMP unreachable.
00:31:59
What's a dirt Bay, I can happen.
00:32:02
In the forefoot thing that can happen is you get nothing. So this is a firewall not being nice at all the firewall stopping the packet. Right. So this means firewall is dropping.
00:32:18
Packets
00:32:20
And note that there's some key terms here. There's some very key terms here I'm using the first time he has it. I'm using a reject we check means
00:32:31
It's a very nice way to respond saying you can't get to the sports or you can't get to this IP address right that's Reject, reject is a nice way to say that.
00:32:44
No response the firewall is dropping the packet as an dropping means it just goes in the trash can. Right, so it comes in.
00:32:53
And the firewall or whatever sees it and says, wait, we don't want. We don't want Alice going to NYU. I'm just going to drop the packet as an no response, just not gonna say anything at all. Nothing. Just, just drop the packets and you get no response at all.
00:33:13
So,
00:33:15
These are the four things that could potentially happen when you do a TCP TCP syn packet
00:33:25
Right, the four things, the four things that can happen is, first thing you get a TCP SYN ACK back. Second thing.
00:33:37
You get a reset.
00:33:39
Third thing you get ICMP unreachable fourth thing, you get nothing.
00:33:46
So let's let's summarize that one more time so
00:33:51
Possible responses to TCP
00:33:56
syn packet
00:33:59
On port.
00:34:02
On a port.
00:34:05
Right stuff for possible responses are one is
00:34:11
TCP sync.
00:34:14
A second and second one is TCP reset.
00:34:23
Or responses I see em P unreachable.
00:34:29
And fourth one is
00:34:35
No response.
00:34:45
So,
00:34:48
I just going to add a exercise right now. Maybe I go into this later on, but hold on let me double check that.
00:35:03
Right, so
00:35:10
Exercise. Exercise. Exercise.
00:35:15
Number eight.
00:35:19
What is
00:35:22
What is the purpose, what are
00:35:27
All the possible reasons that
00:35:33
Each response.
00:35:38
Is returned
00:35:44
So what all the possible responses.
00:35:48
That this whole these responses for occur.
00:35:56
Right. So let's take, let's take three minutes to do that. Right. So for each of these tell me all the possible reasons that you can possibly have the response. So for example, you send a TCP SYN ACK, but all the
00:36:12
possible reasons that you receive a excuse me, you send a TCP syn packet. What are the reasons that you get these pieces act back. I actually, this one's easy. It's only one there's only one possible reason
00:36:24
It's only one possible reason here hopefully other reason about other ones right well all the possible reasons.
00:36:31
For this, so let's take three Minister there for these three items then afterwards I'll be asking everyone to share the answers. If you would like to do that. And if you really feel comfortable you can share it up directly with me as well, but three minutes.
00:38:06
It's been one half minutes. So just not this question is slightly tricky because I didn't go through all the reasons I went to the security reasons, but there are other non security reasons, where some of these answers could come from.
00:38:43
30 seconds.
00:40:05
Okay, stop right there. Would anyone like to share any of the solutions or even part of it. We have it with everyone or just to myself.
00:40:44
Okay, so
00:40:47
First time
00:40:58
So first item this one straightforward, right, number one.
00:41:03
You send a TCP handshake, you get a response.
00:41:07
That means board is open because you're able to send the next packet. Right, so there's there's only one thing that I can possibly mean
00:41:15
Right when you get a TCP syn packet Minister TCP packet and you get into the sink and response.
00:41:23
There is only one thing that you come back point is open right if you send a TCP syn packet and you get a TCP reset it pretty much means only one thing, right, a pretty much means is closed.
00:41:40
But it can also mean firewall is blocking the port.
00:41:48
And well, essentially did the same thing, right, the porters closed and the firewalls blocking the port, it's essentially the same thing right kind of right kind of the main difference is that
00:42:02
When you get reset and the port is closed from the host it means there's no service running from other services not working properly or something like that. So that's fine.
00:42:11
But if the firewall blocking the port, it means that potentially you could have something working as well. You can potentially have something be
00:42:23
behind the firewall that's open. For example, the end when hear about the RDP one ability that came out about last month. It's the blue coupon ability and it has to do with RDP RDP port 3000 something, whatever.
00:42:45
Oh, for example, if you send a TCP syn packet to the RDP port. You could get a reset act back even if the port is open because some firewall has blocked that port up so you can't use it.
00:42:59
So you get TCP reset act. Basically it means a port is closed, but the firewall could be involved as well the firewall could be blocking it as well. So there could be a firewall in place.
00:43:13
Right ICMP unreachable ICMP unreachable basically means two things right. First thing is firewall is rejecting
Unknown Speaker
00:43:26
Packet
Phillip Mak
00:43:29
The first reason
00:43:31
The more common reason is that network problem.
00:43:35
Right. They also means that as well. So, it essentially means two things I see unreachable is firewalls rejecting packet or there's no problem.
00:43:47
And then no response. Well, no responses basically firewall problem by excuse me firewall is dropping.
00:43:57
Packets
00:44:01
Now,
00:44:03
If there's a network problem, usually you don't get no responses like usually you can ICMP problem. But yes, it could be a network problem.
00:44:14
But no response. Really, typically a firewall got in no way very, very usually now i'm not i'm not going to discount it. Right, I'm not gonna discount
00:44:25
That or latency issue right and it does happen issue that we're releasing shoe store, whatever it is, some network issue right numerous issues.
00:44:38
Right, I'll I will take that as a very lower priority of, you know, what could possibly happen but no response, usually means the firewall is dropping the packet right and you can test it out right you can you can test for these things right, especially the network issue, you could send
00:45:00
Multiple
00:45:03
Packets to see if it's a network problem.
00:45:10
With a we keep sending packets. You're supposed to get something back the network working properly. You're supposed to send something back so you can send three Pakistan, Pakistan, just keep trying to see if you get something
00:45:22
Back with it. So here the four possible reasons so we we looked at this from two different angles. So first angle is you send TCP syn packet. What do you get back
00:45:34
And you get back, you know, these four possible responses and also
00:45:41
You get these potential
00:45:44
reasons for why these things occur. And a lot of it has to do if I was
Unknown Speaker
00:45:50
Right, so
Phillip Mak
00:45:54
Even though this is a exercise all diva here.
00:46:03
The next thing I want to talk about is a sink scare. Excuse me. A x can
00:46:17
And I know I jumped. I kind of jumped ahead a little bit, but let me just go through this first
00:46:24
So let me copy some of the slides over
00:46:34
So,
00:46:36
Let me delete this part.
00:46:40
So let's say I do something weird right let's say I let's say I send a TCP packet
00:46:49
Just a TCP packet
00:46:52
You know prior communications.
00:47:00
Do you know what's supposed to happen here.
00:47:03
Like, like what's like what's supposed to happen here when when NYU gets a weird packet right a TCP packet, because the first packet from Alice
00:47:13
From to end my you should always be a TCP syn packet right the TCP syn packet, where a TCP packet. It only has a sync flag said that is the first communication level for a packet. That's the first one is always the first one.
00:47:33
So that's a TCP syn packet. What if the first packet is not just to be safe.
00:47:40
What happens like. So let's say you Sunday TCP packets
00:47:45
And why you what is and why you're supposed to do with that. Like, how, how, how are they supposed to respond to this TCP packet
00:47:56
Yeah, yeah. Reset.
00:48:08
Right, I'll send a reset packet back
00:48:12
Of course, that's normal, right, that's normal.
00:48:17
Communication if everything was working normally do that.
00:48:28
This, this is normal.
Unknown Speaker
00:48:47
This is normal.
Phillip Mak
00:48:52
But what if there's a firewall to place
Unknown Speaker
00:48:57
So there we
Phillip Mak
00:48:59
Just copy this over again.
00:49:06
Now, if there's a firewall and no way and it was my firewall picture.
00:49:13
It is a firewall. Let's say there's a firewall, in a way.
00:49:17
Like typically
00:49:20
How does it firewall react to a TCP packet and the response is different. Right, so I will give you my answer right although I'm asking this question.
00:49:29
I'm gonna give you the answer. Anyways, when a firewall sees a TCP packet
00:49:35
It says, Wait a minute. No one is should be sending a TCP packet. Right. No one right when you send a TCP packet is an attack right. Something is going on right and a typical response I could be multiple responses, but a typical response when it sees this is nothing
00:50:04
Right. And of course, this depends on configuration and it can be configured to reject the packet instead of dropping it right so if I walk can become very good to just
00:50:16
drop the packet instead of, you know, rejecting the packet. But in most cases when a firewall sees a TCP and coming to it. It says, Wait a minute. There's a tack on no one sends a TCP packet is the first packet that doing something weird here.
00:50:36
Doing something weird
00:50:39
Here. Something is going on here.
00:50:43
So this helps you try to figure out what's going on. Right. No one normally was in a TCP packet over so trying to see what it looks like.
00:50:56
Will give you like some idea what's going on. So if I get this. If I get some the TCP act and I get TCP reset. Okay. I can't really told us the firewall in place and not, you know, I just don't know.
00:51:11
But if I send a TCP packet and I get nothing back. Wait, that by itself doesn't tell me anything but so it's a two step process is a two step process. So let's say I did two things like how do I use
00:51:27
How do I use a TCP packet. So the first thing I do is, oh let me makes a little bit more space.
Unknown Speaker
00:51:39
Space here.
Phillip Mak
00:51:43
So let's say I do something else.
00:51:46
Let's say I go and
00:51:51
Let's say I do. Let's say I go Sunday TCP syn packet right I sent a TCP syn packet to NYU, I get a TCP reset right so that's normal, right. So that means the port is closed.
Unknown Speaker
00:52:10
Right, that that's the point is closed.
Phillip Mak
00:52:13
All right. Alright. Okay. Got it. Alright, that's fine.
00:52:17
But then
00:52:20
I send another packet a TCP packet and and then you get nothing back. It says, Wait a minute, wait a minute. So I sent a TCP syn packet to and this is port specific. So let's say port destination port 80
00:52:41
Let's say I do that I got TCP reset Denison a TCP packet and this is also of course specific
00:52:49
This is a
Unknown Speaker
00:52:53
Fourth at
Phillip Mak
00:52:58
All right, and you get quizzes and then you get nothing back so he's he's missing packet and you get like a TV reset act back then you said another packet a TCP packet and you get nothing back
00:53:16
Right. So what does that mean, it means firewalls and away, right. So from here, from the first step. Step one.
00:53:27
You don't know. Right. You say, okay, well I guess it looks like port 80 to close on it. But then you go wait a minute when it's send a TCP packet I get nothing back. So this means by using these two things together.
00:53:44
I know that there is a firewall in place, because when you send a TCP packet. You're supposed to get a TCP reset back not nothing. So, usually a combination of these two
00:53:58
Really helps me and tells me that. Wait a minute. This tells me that there's a firewall in place or doing something right. So the big thing about Sunday TCP X is that TCP acts are not used by themselves. This is so important. I went right down here, right. So TCP x
00:54:18
Are
00:54:20
Are not helpful when used alone.
00:54:27
When
00:54:28
Not used in conjunction with a nother scan type
00:54:38
Right. So in this case, it turns
00:54:47
Out that there
00:54:52
There is a firewall that makes port ad
00:55:00
Closed
00:55:03
Port ad may be running behind
00:55:10
The firewall. We don't know yet.
00:55:16
So this is that important. So TCP X scans, never to be used by themselves. It doesn't tell you any information.
00:55:26
About it, when you do it by itself. It's something that you need to us together. So I send a TCP sync, I get, let's say this
00:55:36
You get used to be reset. Okay. That doesn't tell me anything. But then I do a TCP act on it and I get nothing. Wait a minute. This is a file. There's a firewall in place here.
00:55:48
That's doing something weird in this place. I remember firewalls. They work by IP and port numbers. So, you know, if I was can be blocking one port, but not another one right so that's information that you really need to understand firewalls work by by port numbers as an IP addresses.
00:56:09
Hope. This is how a TCP act sending a TCP packet can really help you try to freak out what's going on in the network.
00:56:21
So these notes will be available after class. There we go back to our slides. So I think we jumped ahead a little bit, but that's okay. That's all right.
Unknown Speaker
00:56:32
Where am I
Phillip Mak
00:56:34
Okay, so you should be seeing your main slides now so we talked about TCP three way handshake.
00:56:44
We talk, we're gonna talk about n map and map is a extremely popular open source port scanning tool was in the movie The Matrix.
00:56:54
And and map has a lot of scan types, allow them cool dude just some of them. This is something that you need to know. Right.
00:57:03
It's, you don't need to memorize it, you really do need to know it right because because you can get a question on any of these things like an exam.
00:57:13
Oh, this is too easy, right. A question on how one of these scary entire tour. That's really, really easy for me to write. It's something that you should know. It's very easy to grey just really good questions on the exam.
00:57:30
So the first type of scan the app does is the TCP connects scan the TCP connection is, well, it's, it's essentially exactly what we're talking about the whole time. So the TCP connect scan is where you have
00:57:48
You know you have Alice on the left side you have the NYU and you do a TCP
00:57:58
You do a TCP syn packet, you get a TCP
00:58:10
TCP whatever back but then a tissue a tissue connect scan it also closes the connection as well. So after establish the connection. It'll send a TCP Finn, and then you get a TCP fintech as well.
00:58:29
So it's a TCP connects can it's TCP connects scans are expensive, right, and they're expensive because it takes a lot of packets. So I guess I missed the point that when you do a TCP
00:58:41
TCP syn packet you do to be sink sink sink at x Finn Finn know before you close the packet. So it's a lot of packets to do
00:58:56
A TCP sync scam.
00:58:59
Is much faster and TSP sinks can always send a reset know battle, but the point is open. So let me go into some examples here. So let me go back to my notes slide.
00:59:16
One WOMAN'S RIGHT HERE YOU GO.
00:59:24
I don't know, there's a wrong slide.
Unknown Speaker
00:59:28
Here we go.
Phillip Mak
00:59:32
Here we go. So let me go back here.
Unknown Speaker
00:59:43
I want to talk about
Phillip Mak
00:59:45
End map.
00:59:48
Conduct scan.
00:59:52
Versus sync scan.
00:59:57
Scan
00:59:59
What we have
01:00:04
What we have been talking about. So it's Candace, the
01:00:12
Is this one. So this is a connect scam.
01:00:20
Just a tiny bit smaller. So we have more room to write other stuff.
01:00:47
Okay, and then afterwards, after it establish the three way handshake.
01:00:53
It sends a
01:00:55
TCP Finn.
01:00:59
Did you get a
01:01:02
Good Finn.
Unknown Speaker
01:01:07
Finn.
Phillip Mak
01:01:10
So, it connects scan it's expensive.
01:01:16
Right, it takes five packets to, you know, go through it, at least at least five packets, but a TCP sync scan.
01:01:28
Is also called a half open scan and it's much faster as much faster because
01:01:33
No matter what, I'll just close the packet. So a TCP
01:01:41
There you go, a TCP sync scan already has a maximum of three packets
01:01:51
There you go. That's it. So there it is. That's the only thing there is to it.
01:02:01
So I TCP sinks can be built this down.
01:02:06
So, this side is a sink scan and on top here is a connect scam.
01:02:15
Since can just sends a TB sank. He gets he basic act back to speed Lisa will just reset it say that so the maximum of three packets when it's open.
01:02:25
Or just two packets when it's close. So a six scam is much, much faster than it connects scan and connect scan uses the operating systems API read this one uses the operating system API. So you don't even need admin rights to it uses
01:02:47
API to do it. So it's very easy our sink scan it writes his own libraries. It does have its rights directly onto the network and do whatever it wants. So since get is much, much, much faster, like an order of magnitude faster. So that's a sink scam.
01:03:17
Hey, so the next thing is a fin scan a TCP fin scan and for us. We're not going to really talk much about it, but what this means is that a TCP header and we do we have picture TCP header here. Yeah, here the TCP header, not as IP header.
01:03:39
Well, a TCP header has a number of flags on it. So if you if you send a TCP packet with just the fin flag set, it will well
01:03:53
Usually, it should send a reset.
01:03:58
Actually, it should send a reset, no matter what. But a fin scan is just another way of manipulating the packets in order to get a elicit a response back to it.
01:04:11
And n map and online, you can have a reference of what each of these operating systems are supposed to respond to different flags or a set or not set
01:04:25
Another attack another scan type is called the TCP know scan attack and no scan.
01:04:32
Will
01:04:34
Send a TCP packet with no flags whatsoever and you get different responses, depending on what the operating system is
01:04:42
TCP scan.
01:04:48
Scan yep you just that we just discussed it. Oh, I missed, I missed one possible response. You haven't here.
01:05:02
Oh, I missed the response. Yeah. Here we go. There we go back here.
01:05:08
So a TCP
01:05:11
X can so you can also. So I said, a TCP X. Can we turns out that you can also you can also get a ICMP ICMP unreachable.
01:05:25
But that's, that's where it's it's rare.
01:05:29
Right, and it's it's where because
01:05:33
Firewalls know that if we take a TCP packet, you're probably under attack or some packet is no Soviet. You don't even need to respond to it. That's a TCP packet. So if you could get an instrument reachable but it's really, it's, it just doesn't normally do that. But regardless
01:05:59
You tend to TCP your sentences to be back. You get a reset. If there's no firewall. If there's a firewall, you could get something else like nothing or an ICMP unreachable.
01:06:16
Right, so
01:06:19
What are the skin types on their
01:06:24
excess skin eczema scan is when you have all the flag set
01:06:29
FTP bounce scan attack. We'll talk about that version scanner and map has ability to scan full version numbers inside
01:06:38
Of programs and protocols and such fragmentation. Can the fragmentation scan is to fragment packets into multiple fragments and see how an operating system for service respond to it.
01:06:55
TCP sequence production, right, we're talking about later.
01:07:01
Right TCP three way handshake. We talked about this already.
01:07:05
talked about this already.
01:07:08
Exercise to spend two minutes on this.
01:07:15
And let's take three minutes on this and I will take a break during the spring minutes as well. So exercise. Number two, what information can be obtained from a an app sync scan. Let's take three minutes to do that.
01:09:37
10 seconds.
01:10:32
Okay, so
01:10:34
We pretty much gone through this already. So please submit your answers.
01:10:42
UDP UDP is well it's it's much simpler than TCP. This is what UDP header looks like you see that it basically has nothing in it so UDP header has source destination port.
01:10:59
Are has the length of the entire payload to check some and the rest of it is just information. It could be anything as well.
01:11:23
So perfect right so the answer in the chat room. Perfect. Right.
01:11:29
So UDP is pretty simple.
Unknown Speaker
01:11:34
But
Phillip Mak
01:11:36
And how UDP works is, essentially, you send a UDP request, you get a UDP response.
01:11:45
Can this can name a name. A popular UDP protocol for me.
01:11:51
That you're familiar with, like any popular yet DNS DNS port 53 qu IC not familiar with that, let's take a look at that later.
01:12:02
D and s port 53 right so the end. So it's a very popular.
01:12:09
UDP packet and how that works is
01:12:14
You send a UDP packet source port some number greater one or two or three destination port 53
01:12:24
You send a packet to
01:12:30
Is that correct, double check that it would make sure I would check that.
01:12:48
I think DNS requests or from
01:12:53
Right DNS requests are from 30 to 53 not sure about that. I did double check what that is. I think it might be right. The DNS is one of those weird ones that does that.
Unknown Speaker
01:13:07
Oh,
Phillip Mak
01:13:13
Oh, you send a UDP packets to port 53 DNS, you get a DNS response. So you get DNS response. It means the port is open, you get a response. It's open.
01:13:28
Or if it's closed. You can ICMP unreachable. See, here's the thing with UDP. It's UDP ever is closed. You can ICMP unreachable. You don't get UDP packet back, you get ICMP unreachable. But then, but then the third possible option is you send a UDP packet, you get nothing back
01:13:53
And that's the big question, you send a UDP packet, you get nothing back
01:13:59
What does that mean if you get nothing back
01:14:05
Right. What does that mean well
01:14:11
It could mean several things. First, you know, that could be a network problem you can get something back or he's too crazy about crazy thing about DNS. It's not that crazy if you send a DNS packet to port 53 but you mess up the packet somehow
01:14:31
It won't respond if anything at all. So, for example, a another popular UDP packet is the HTTP. So let's say you send a DAP packet to DNS ports.
01:14:44
You will get nothing back if you get in properly formatted UDP UDP packet and you send it to port 53 you don't get anything back so
01:14:57
Meaning you unless you know that that port is for DNS and and you send a DNS packet to port 53, you're not going to get anything back. So let me say that again.
01:15:13
Yes, runs on port 53 but if you send a packet to port 53 if you send a DNS packet, you get a response.
01:15:24
So the EDP response.
Unknown Speaker
01:15:27
But
Phillip Mak
01:15:28
If you said if you miss format or UDP DNS packet, you get nothing back if you send the wrong thing to the port 53 we don't get a response back in order for DNS to respond on port 53, it has to be on the correct format packet also doesn't respond anything at all. So in other words,
01:15:54
If you send a UDP packet to report.
01:15:58
And you get no response. It could mean the packet got dropped
01:16:03
It could mean a firewall is blocking it
01:16:07
Or it could mean you have improperly formatted packet
01:16:13
So I you can't figure out what is so the secondary example.
01:16:20
Let's say you know port 40 had is open on UDP what 49 supports what what you do, what UDP service runs on port 40 I have no idea, but I tried to figure out in western a DNS packet to port 40
01:16:38
The no response.
01:16:40
It means I don't know is a firewall blocking it did I send the wrong protocol to it. I don't know. So that's one issue with UDP, that's one issue. The second issue.
01:16:55
Is that these ICMP unreachable.
01:16:59
window is closed, they only get return one per second.
01:17:06
Meaning
01:17:08
If you send to the UDP packets per second, you only get one ICMP response one ICMP unreachable meaning. The point is close. In other words,
01:17:21
You cannot send UDP packets more than once per second on a Linux machine or two per second on a Windows machine, it makes a difference. So it's one per second.
01:17:33
But he's centrally to scan UDP, which is how many ports 65,000 ports and you only scan one per second.
01:17:46
That will take 65,000 seconds in order to scan to all the UDP ports on one host
01:17:54
That takes a long time.
01:17:57
That takes that takes a long time.
01:18:01
And the other problem that only does is take 65,000 seconds to scan UDP on one host
01:18:10
Unless you you know what's running on the service. You can even figure out what the point is really open or the firewall way. So it's let's say someone moves DNS port 53 to portrait before, for example.
01:18:23
And you don't know that and you send something to port 54 on let's the DNS packet, you won't get a response at all.
01:18:33
So that makes UDP scanning really, really hard. So those two main things. Those two things right. The two things being
01:18:43
You only scan once per second. And the second thing is you have to have a properly formatted packet in order for it to respond.
01:18:53
Make scanning UDP really, really, really hard. It's so hard. That's typically not done at all.
01:19:04
Or maybe just the top 100 ports or something like that is scan. So if you if you are like the bad guy or the Bad gal and you want to do a run some service on
01:19:16
You know, some something listening on the host, you should run it on UDP right some weird UDP port because no one is scanning for these ports is really, really tough to scan from the outside the UDP port. It's just really hard. How do you do it.
01:19:39
How do you do it, but you can't, right. You just, you just can't do. It's way too hard. You can't scan it from the outside. So essentially, you don't scan UDP. Right. It's just too hard to do because of these problems.
01:20:01
Scanning purposes of X guy needs to check for firewalls.
01:20:06
FTP bounce can FTP bounce ganzel really really interesting type of scan, it's, it's something that's built into n map and it's it's just so weird.
01:20:17
But a map can do is, and map will find FTP servers to allows numbness logins on it on the internet. So you can scan for and see
01:20:28
If there's any FTP servers that allow you to log in with our username and password or username being anomalous and actually it's they still exist even today, they still exist on the internet and a map has a scan for it and try to scan for these things.
01:20:47
So, let's say, is able to get on the FTP server and map can use man's on the FTP server specifically there a CT command.
01:20:58
And the port command attempts to transfer file to a nother target on a particular point number. So, for example, it can try to send it on port one and see if the if the
01:21:12
Point is open or not for to see other ports open it up for three see the ports open it up for for pseudo ports open to that. So it just keeps doing that over and over and over again.
01:21:21
And essentially an FTP bounce can allow the attacker to log into FTP server and scan targets from the FTP server, meaning
01:21:33
They have no idea that they logged in to do anything right this target here has no idea that the attacker who the attackers, the target here sees that the scanning activity is coming from the FTP server.
01:21:49
So for example, in the last two days you've seen me performing reconnaissance on and why you
Unknown Speaker
01:21:56
edu.
Phillip Mak
01:21:58
I have not personally sent a single packet to NYU. I mean, doing my scans. I mean, I'm an agenda, you now, but through my scanning activity. I did not send a single packet and my you
01:22:15
They may be able to see that someone's scanning them, but they don't know who's doing it and they definitely don't know that I'm doing it because I am not associated with any of the backers I sent them.
01:22:32
IP.
01:22:35
IP header. So this is the IP header. This is something that you should be familiar with. It's required for you to be familiar with this class. But one thing I will point out is the IP ID here.
01:22:47
The iPod.
01:22:50
And the IP ID is a 16 bit field use for the purpose of off fragmentation and reassembly reassembling. So what this means is that if an IP packet becomes too big. Right. And it's bigger than know whatever is allowed, which is 4000 bytes or something like that.
01:23:15
It gets fragmented and all the fragmented.
01:23:18
Pack gets have the same IP ID.
01:23:26
So,
01:23:30
The IP ID is supposed to be a random number every single time. Right, so every time, every time I pack and I get back is sent out from a host. It should be a random IP ID.
01:23:45
But the thing is, it may not be random right some really, really old host don't have a random IP ID, for example, Internet of Things items they typically use a very older version of the next where they just grab a weird flavor. It doesn't get updated that often.
01:24:08
And they could have issues, just like this and IP ID that increments sequentially is supposedly random, but sometimes the next packet will have one IP ID.
01:24:21
Of the problem and that leads to have one ability that can be exploited.
01:24:29
The one ability that can be exploited. A is called the idols can and here's how the idols can works here on the left side that's attacker. All right. That's the bad guy true data attacker.
01:24:43
And on the right side is the frame machine to machine. It's being framed here and a target. Here is the one that you're trying to scan. So he is how the idol scan works. And this is the end map idol scam.
01:24:58
Is n map.
01:25:03
I go scam. It's a scam feature of n map.
01:25:09
And here's how the scam books.
01:25:14
Step one.
01:25:16
To two feet, the attacker sense a TCP syn packet to defame machine.
01:25:22
The frame machine replies by forcing that the frame machine with just a one that has a IP ID that increments. One bite at a time has an IP idea of let's say x
01:25:37
Then the attacker.
01:25:40
Sends a packer to target. So it's booths is a dress to say a came from.
01:25:52
To say that came from the frame machine.
01:25:55
So the target replies back through the TCP syn packet to the frame machine. So essentially the target is sending a TCP sink back to the frame machine.
01:26:09
In the famous she responding back to the TCP SYN ACK with a reset back
01:26:18
And back and reset back and it's an IP ID is
01:26:24
Increments by one
01:26:27
Then the attacker will send another pack number seven Sunday sink back into the frame machine in the same machine will respond back the frame machine will have an IP ID plus two. Since IP ideas plus two, that means the port on the target machine is open.
01:26:48
I know there's a little bit complicated. Let's go over that one more time.
01:26:53
Because make some notes here where where I here it is so new slide. This is the an idol scan.
01:27:10
And I have three of them here. So on the bottom left corner. I have the attacker.
01:27:22
Okay, on the bottom right corner. I have the
01:27:27
Victim
01:27:31
And on the top. I have the innocent bystander.
01:27:52
So,
01:27:54
Here's how it works. Hold them because because of arrows from here.
01:27:59
So attacker.
01:28:02
And say TCP syn packet to the victim.
01:28:07
The victim.
01:28:12
Will send a packet back and a packet will be
01:28:25
TCP sink back or like a PVC.
01:28:33
With IP ID equals x.
01:28:39
Alright.
01:28:41
And the doctor.
01:28:45
Will send a packet
01:28:48
To the innocent bystander.
01:28:52
And this packet is
01:28:56
TCP syn packet and it has a source IP.
01:29:02
And destination.
01:29:07
IP the source IP is see it says it's it's coming from attack of what's actually from the victims were saying it's a victim. So it's booth.
01:29:20
And destination IP is the innocent bystander acquired
01:29:27
That's just court I for innocent bystander.
01:29:32
Innocent Bystander
01:29:35
Received this packet and says, well, actually, my point is open. So, it responds back but it thinks is responding back to the victim.
01:29:51
responding back to the victim. So, it responds back to the victim. So TCP sync act and stores IP is I and destination IP is
01:30:09
The right so the response back and the victim says that's a reset got a sick act and it goes way, the minute
01:30:19
What does this mean
01:30:21
What does this mean
01:30:28
It says, wait, something's wrong. He asked, and they said a TCP reset.
01:30:35
High and the TCP reset will now have an IP i t it goes x plus one.
01:30:53
All right.
01:30:54
Then the attacker was send another request over the attacker.
01:31:01
Was a nother
01:31:04
TCP syn packet over
01:31:10
And the TCP sync and the victim respond back with
01:31:19
TPS TCP IP ID equals x plus two. So when you get this response, it means
01:31:28
The innocent bystanders.
01:31:33
So this means that x plus two means innocent.
01:31:39
bystanders.
01:31:42
Or is open.
01:31:57
Alright.
01:32:00
So,
01:32:03
Exercise. So exercise be
01:32:15
How does this diagram change if
01:32:21
The it is sent.
01:32:25
By standard port is closed.
01:32:39
Exercise number be
01:32:42
How does this diagram, change the innocent bystanders port is closed, let's take two minutes do that and then afterwards I'll ask if anyone like to share the answers.
01:32:54
Let's take two minutes.
01:34:56
Like to share the answers with the class.
01:35:34
Right one main thing to change is the main changes since parts here if this becomes a if the port is close to get a TCP
01:35:47
Reset.
01:35:49
And what the, what do you respond over TCP reset nothing right so nothing
01:35:58
Nothing. You don't respond anything right you don't respond to be reset.
01:36:04
All right, there you go. So this part.
01:36:11
This part here.
01:36:15
becomes x plus one.
Unknown Speaker
01:36:22
Plus one. There we go.
Phillip Mak
01:36:31
There we go.
01:36:33
So that's the major difference here.
01:36:43
Idle scan.
01:36:47
And map also has commands us for fingerprinting so in your lab I think lab to you have always finger you have a number of n map tasks to do. And one of the past is to perform always fingerprinting
01:37:02
There are a lot of Ed good commands in this chart that will be helpful for lab to now be
01:37:11
Given out after next week, or will be do after next week was not released yet so
01:37:20
This chart is really, really helpful in helping you with performing a lab assignment. It gives some really good commands, such as
01:37:30
Dash as fee will give a service scan it will give version information for the course that you get or dash as capital C which is script scanning. I mean, they will disrupt scan or
01:37:45
Other good ones. He. Oh, I think that's a good ones here right dash capital. Oh right, detect the operating system right some really good commands here.
01:37:56
File walk Fire Walk is
01:38:01
Fire Walk is similar. It's like trace route upset for application data so you understand how trace route work trace while shoots and ping package with a TT L that is
01:38:19
That decreases one at a time.
01:38:22
But that's for pings file walk is the same thing upset. They use application data and you can do that for anything you send the application data like a TCP syn packet or something like that and you just have a TT out that you know you we do one at a time until you figure out
01:38:41
Information about the network that's file walk. It's a trace route for application data.
01:38:49
There are other tools out there, such as HTTP recon and such and HTTP recon is really good only because it
01:38:57
It knows web servers, like it and knows information about web servers and your fingerprint them and find out information about
01:39:05
You know, whether it's running at pat chair or what kind of files are running on it. It's some pretty good one and this is an old one. So, too. I don't remember the name right now.
01:39:14
Oh, Vegas Vegas another one. It's kind of like a vulnerability scanner, but Vega can be used for identifying web servers as well and Vega. Also worth of custom web apps.
01:39:29
Oh, at this point we have walked through all the steps off the network reconnaissance
01:39:41
Mythology. So we start with collecting open source Intel, then we perform that we're scanning host scanning and port scanning
01:39:50
After that you get all there together and try to analyze it and tried to figure out what is it that you're looking at. So at this point, you see from the notes that I got a lot
01:40:01
I have a lot of information but NYU. You tried to put it together and try to understand how does the NYU network look like. Like what is in there.
01:40:10
They tend to forget. And it was any areas and define what information in core and reach out and find more information in the last type of recursion.
01:40:23
Exercise number three.
01:40:27
It's a review, what are the possible responses to a TCP sync scam. How about a UDP scan right let's take two minutes to do that.
01:40:45
And for this one I will not be asking for responses. Just keep the doors for yourself.
Unknown Speaker
01:41:48
The
Phillip Mak
01:42:40
Start right there. We're going to move on. So now we're up to lectured three. So we are likely behind schedule and that's okay right so lecture three so up to electric three slides right now. And what you will learn in luxury three is
01:42:59
Understanding why it's so hard to stop spoofing
01:43:06
You'll talk about the different ways to exploit systems learn a lot. But the DNS systems, even more than we're talking about medicine. Right. And, you know, learn how to use split or a very rudimentary level of medicine right
01:43:23
So systems have a lot in security. Right. And they come from all over the place.
01:43:32
And there are lots of ways in which systems just are not secure
01:43:38
So, for example, one way they need to be insecure is just by not patching windows patch Tuesday comes out every Tuesday.
01:43:47
And they need to be patched. Right. That happens all the time, right, every patch Tuesday second Tuesday of the month, more windows patches come out and if you don't patch it
01:43:59
You become insecure. But there's other ways that you could be insecure, for example, standards standards can cause you to be insecure.
01:44:10
Like for example eaten eaten at the layer to protocol has lots of insecurities in it because eaten that was designed at an age where
01:44:20
You didn't people are not concerned about security, right, or Bluetooth by Bluetooth was designed without much security in mind. So Pluto originally was not secure. So if you decide to use Bluetooth, you have these insecurities.
01:44:37
Requirements requirements are things that you need to build your product to and requirements can cause and securities as well.
01:44:46
So for example, if the requirement is that users to be able to log in, without typing in the past for passwords one and once a day, that is a requirement. They'll cause and securities.
01:45:01
Architect architecture right the way that your network is set up causes insecurities. So example of an architecture insecurity would be that your network needs to go through certain points that are not secured.
01:45:17
And because of that, you just inherit insecurities in your network. So you can see how there are many, many ways that you can be insecure, one of the one of the most important things
01:45:32
Cause and security is configuration or configuration management like not configuring your systems correctly has vulnerabilities. It causes things to be insecure.
01:45:44
So for example, let's say you set up a new box. A new Windows box you do that you already have insecure things right off the bat.
01:45:55
Right, you open. Let's say you booted a oracle database and Oracle database has default administrator account and default backup administrator accounts. The first day, you gotta do is go and change that if we don't change it, you have issues so
01:46:16
There are there are guides out there to help you figure. So if you are installing a database if your security administrator and you didn't start database.
01:46:26
First thing you do is you go find a guide to to securing or go and go run to the checklist to make sure that the oracle database is secure.
01:46:37
And for everything that you install, you have to go find a security configuration guide and forgot what exactly what settings and necessary.
01:46:49
In order to ensure that is it secure. And this is something that you can use a judgment call based on your environment such but for pretty much
01:46:57
Every single product and every piece of software out there, there is a security configuration guy you go look that up. Find it and just follow the guidelines as a starter of what to do because
01:47:10
You cannot just take it out of the box and run it is not secure and somebody that's so easy to fix.
01:47:23
Configuration security we just discussed this exercise number four.
01:47:30
Opponents your security engineer for large enterprise that work, how would you ensure that stuff when a host or configure security.
01:47:39
How do you ensure that they remain configured securely. I'd say two minutes for this question and then I will also ask you for your responses.
Unknown Speaker
01:48:55
20 more seconds.
Phillip Mak
01:49:45
Where anyone like to share their responses. The class.
Unknown Speaker
01:50:03
So,
Phillip Mak
01:50:06
I want to take windows, for example, Windows. Windows has a massive number of configurations and let's say you're a security professional and you you ensure the Windows system is secured properly right you'll follow Windows security.
01:50:23
Guide to configure it correctly, and then
01:50:27
So now the host is configured well
01:50:31
Then you have to make sure that it remains configured well as well. Let's go options that you can do. For example, you can lock it down.
01:50:39
And lock it down. Such a way that user can change the settings. But another thing you can do is that you can have some agents can the host every once in a while and make sure that it really still to configuration that you said continue to
01:50:54
Be the way that you meant it to be right. So it's really important that you do that.
01:50:59
In a large that work otherwise knows the host will start drifting away from what a secure configuration is and you have deviations from a secure baseline know all over the place and it's a hard part is off.
01:51:19
School spoofing
01:51:21
So let's say
01:51:23
You have a normal, you know, IP communications upset this House, which is like 145 13 send the packet to this House, and I know we talked about spoofing so easy, but
01:51:38
Spoofing is never easy. Um, so, how easy is it for you to spoof your IP address and can you get response. So exercise number five. Let's take one minute do this how easy it is for you to spoof your IP address and send a message and kind of reply right how easy it is to do this.
01:52:01
Let's take one minute and I'll ask you to share your answers with the class. If you want to
01:53:01
So,
01:53:04
How easy is to spoof IP address and you send a message. So, for example, can use change IP address right now and send a message like don't do it right now because you're lose connection with the
01:53:18
With the server for this class, but can you do that, like, can you just change the IP address right now and send a message out.
01:53:31
Can you do that.
01:53:33
Is it possible
01:53:37
To do that.
01:53:41
And well, the answers yes. Now you can change your IP really really easily.
01:53:48
And just get a reply back. You can do it right now. Like, not right now, but you can do it. Just go to IP config or if config and just change IP address, you can do that and it'll still work.
01:53:59
Is really really easy to change the IP address is really, really easy to spoof your IP address is something that's completely trivial, anyone can do it.
01:54:12
And the reason for that is that these hosts that these network devices they can accept it, right, the dumb devices that can handle these things. So it just really, really easy to change it in one of our future labs, you'll be writing a
01:54:30
You'd be running a script using Python in order to fake your IP addresses. It is really, really, really easy.
01:54:41
Right, that's the end of this class for last exercise. Please make sure you put in your model points as well. So there's anything from today's class that are, that is not clear to you, please let me know.
01:54:53
In your submission. Alright, that's always the last thing for the exercises. Again, thank you all for being able to join me live for those you can please make sure you watch the video and answer the questions before the next class.
01:55:06
Also, if you did not get on Slack yet, please make sure you do that immediately. Thank you very much. And I hope everyone has a great week, take care. Bye. 
