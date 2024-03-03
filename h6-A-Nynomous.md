# A. Nynomous

## [Quintin 2014: 7 Things You Should Know About Tor](https://www.eff.org/deeplinks/2014/07/7-things-you-should-know-about-tor)

Summary:

1. **Tor Still Works**: Despite attempts by organizations like the NSA to compromise it, Tor remains effective at providing anonymity. Most attacks on Tor involve exploiting browser bugs or user misconfigurations, rather than breaking its cryptographic security.
2. **Tor is Not Only Used by Criminals**: Tor is used not only by criminals and corrupted groups of people, but also activists, military personnel, journalists and private people seeking privacy. There are more sophisticated tools that criminals can use like botnets with malware or identity theft.
3. **Tor Does Not Have a Military Backdoor**: While it was initialy a US Navy project, since it's open source it has been verified by multiple trust-worthy sources that there is no backdoor for the military.
4. **No One in the US Has Been Prosecuted For Running a Tor Relay**: There have been no prosecutions in US since Tor relay is not illegal under US law.
5. **Tor is Easy to Use**: There are easy ways to to access Tor such as the Tor Browser Bundle, which is preconfigured for safety, or Tails, a live operating system that routes internet connections through Tor.
6. **Tor is Not as Slow as You Think**: Tor might be slower than regular internet connections but efforts are made by engineers to improve its speed. Creating more relays is another way.
7. **Tor is Not Foolproof**: If Tor is used incorrectly it can infact compromise your anonymity. That is why Tor Browser Bundle or Tails should be used, software should be kept updated and services like Google or Facebook should be avoided as they can still see communications within their systems.

## [Shavers & Bair 2016: Hiding Behind the Keyboard: The Tor Browser €](https://learning.oreilly.com/library/view/hiding-behind-the/9780128033524/XHTML/B9780128033401000021/B9780128033401000021.xhtml#s0010)

- **Abstract**

- The Tor Browser, or "Tor," enables anonymous Internet communication.
- It anonymizes users, making tracking or identifying them difficult.
- Forensic analysis may not uncover communication but can yield valuable artifacts.

- **Keywords**

- Anonymizing, Anonymous, Communication, Covert, E-mail, Forensic analysis, Internet browsing, Naval Research, Tails, The Onion Router, Tor, Virtual private network

- **Introduction**

- Tor is a modified Firefox browser hiding users' IP addresses.
- It allows easy and effective anonymity for anyone.
- Tor facilitates anonymous Internet surfing and communication.

- **History and Intended Use of The Onion Router**

- Tor's purpose is to enable anonymous Internet communication.
- It has diverse applications, including bypassing government blocks and facilitating whistleblowing.
- Tor, initially developed by the US government, is now open for improvements by various entities.

- **Two Ways of Looking at The Onion Router**

- Tor presents challenges for forensic analysis due to its unique nature.
- It can be examined forensically on devices or as currently used by suspects.
- The analysis focuses on Windows but applies to other operating systems.

- **How The Onion Router Works**

- Tor routes Internet traffic through random relays, encrypting it.
- Data passes through entry, middle, and exit relays, with each layer of encryption stripped at each relay.
- The final exit relay connects to the user's desired target with an unencrypted connection.
- Tor routes Internet traffic through random relays, encrypting it.
- Data passes through entry, middle, and exit relays, with each layer of encryption stripped at each relay.
- The exit relay does not know the entire traffic route, enhancing anonymity.
- Tor changes routes every 10 minutes, further complicating tracking.
- An analogy of Tor is mailing a letter through intermediaries, with each layer representing encryption.
- The name "The Onion Router" reflects how data passes through layers of encryption, like peeling an onion.

- **A Few Important Points About Tor**

- Tor's network of relays is operated by volunteers, enhancing anonymity.
- The number of Tor users worldwide exceeds 750,000, utilizing over 6000 relays.
- Tracing Internet traffic on Tor can lead globally, complicating investigations.
- Tor circuits change nodes every 10 minutes, adding to the difficulty of tracking.
- The middle relay in a Tor circuit remains unknown to both the origin and destination, reducing suspicion.
- Bridges, unlike public relays, are not listed publicly, making them difficult to block in countries with Internet censorship.

- **From a Tor User’s Perspective**

-The Tor browser is a modified Firefox browser, requiring minimal technical skill to use.
-Installing the Tor browser bundle is simple, requiring about 10 mouse clicks and 10 minutes.
-Default settings are sufficient for most users, requiring minimal configuration.
-Additional configurations, such as using bridges or local proxy settings, may be necessary in countries with Internet censorship.
-Tor provides strong anonymity and ease of use, making it suitable for both legitimate and illicit purposes.

- **So What’s the Big Deal?**

- Tor enables criminals and terrorists to communicate and conduct activities with near absolute anonymity.
- Using webmail services with Tor hides true IP addresses, making tracing practically impossible.
- Tor protects both innocent and criminal communications, enhancing anonymity and encryption.

- **From Your Perspective**

- Investigating Tor involves examining devices or Internet traffic.
- Unmasking Tor is challenging and overwhelming for investigators.
- Legitimate and illicit uses of Tor depend on the manner of use.

- **Forensic Analysis of The Onion Router**
 
- Finding the Tor browser in forensic analysis requires searching for it, often in unconventional locations.
- Multiple versions of Tor may exist on a device, indicating prolonged usage.
- Tor browsing history is not stored in typical locations, requiring memory dumps for recovery.
- Other artifacts like Windows prefetch files and registry entries provide insight into Tor usage.
- External drives accessed during Tor usage may contain suspect files, indicating data exfiltration.
- Despite limitations, forensic analysis of Tor provides valuable information, including historical usage.


- **Tracking Criminals Using Tor**

- Despite its challenges, government agencies are actively working on deanonymizing Tor users.
- A few successful cases involve exploiting errors made by suspects rather than breaking Tor itself.
- The FBI once exploited a Firefox bug to capture IP addresses of Tor users visiting a child pornography hosting service.
- Customization of Tor browser settings can inadvertently leak information, making users vulnerable.

- **It’s Possible to Break Tor!**

- While Tor has vulnerabilities, breaking it requires significant resources and time.
- Various methods, including attacking the Tor network or man-in-the-middle attacks, have been theorized but remain challenging.
- Success in tracking Tor users often relies on suspects' mistakes or external factors.

- **Used in Combination of Other Tools and Methods**

- Tor, when combined with other security methods, enhances anonymity and communication security.
- Tails, an operating system designed for anonymity, offers additional layers of protection and leaves no trace on the host computer.
- Forensic analysis of Tails usage presents unique challenges due to its design to leave no trace on the host system.


- **Related Tor Tools and Applications**
  
- Third-party tools like the Anonabox hardware router route all Internet traffic through Tor, enhancing anonymity beyond just the Tor browser.
- Mobile applications like Orbot enable Tor usage on smartphones, expanding the reach of anonymous communication to mobile devices.
- Hidden services, servers on the Tor network, provide end-to-end encrypted services and are accessed with .onion URLs, making them practically invisible on the regular Internet.

- **Summary**

- Tor is extensively used worldwide for both legitimate and illicit purposes, making it crucial for forensic investigations to consider its potential use by suspects.
- Identifying Tor users poses significant challenges, requiring a comprehensive approach that goes beyond traditional investigative methods.
- Investigations involving Tor often require understanding not only the individuals involved but also the contents of their communications, emphasizing the complexity of tracking illicit activities on the network.


## Install Tor / Access Tor

First I go to this website to download it:

[Tor Project](https://www.torproject.org/download/)

![tor1](https://github.com/PanosArvan/Information-Security/assets/145275148/dff12493-51e1-46f1-bce4-72e848cf80d8)

Then I search in DuckDuckGo while onionized for dark web marketplaces:

![tor4](https://github.com/PanosArvan/Information-Security/assets/145275148/2cdd6af3-a42a-4d19-8d40-68bccc096ef2)

These two websites provide info on a few marketplaces. 99% of them regarding something illegal"

[Marketplace1](https://darkwebmarket.net/)

![tor5](https://github.com/PanosArvan/Information-Security/assets/145275148/e0383d5a-6437-4e9e-9ab8-7b993435d528)

[Marketplace2](https://cypher-marketplace.com/)

![tor6](https://github.com/PanosArvan/Information-Security/assets/145275148/9115371e-f23b-4522-8cd8-cb9f4dc87ffc)

Using the cypher-marketplace I was able to find Cocorico Market, where they sell illegal drugs (NOTE! This is done solely for observational and research reasons within the realm of academic assignments, NO purpose in participating in any kind of illegal activity.):

[Cocorico Market](http://xv3dbyu75coadsrwlbofnsg3dj5axfzcxh5v4nrvtcn3ey7uv6vrf5yd.onion/store/nojs/)

![tor7](https://github.com/PanosArvan/Information-Security/assets/145275148/f2dc8c07-79bb-4115-ae68-43e568cf11f5)

Using the HiddenWiki:

[Hidden Wiki](https://thehiddenwiki.org/)

![tor8](https://github.com/PanosArvan/Information-Security/assets/145275148/97c8a871-550a-4ea3-b291-d9f7d6b725e0)

I was able to find another website that has the same onion links thus allowing me to directly open them from the Tor browser:

[OnionLinks](http://s4k4ceiapwwgcm3mkb6e4diqecpo7kvdnfr5gg7sph7jjppqkvwwqtyd.onion/)

![tor9](https://github.com/PanosArvan/Information-Security/assets/145275148/3e579134-359d-4957-b026-8f880dc59865)

There I found this website:

[Shadow Wiki](http://zsxjtsgzborzdllyp64c6pwnjz5eic76bsksbxzqefzogwcydnkjy3yd.onion/)

![tor10](https://github.com/PanosArvan/Information-Security/assets/145275148/98da7a43-3831-42e2-86a4-af53e10c6c1e)

And this blog:

[MayVaneDay Studios](http://meynethaffeecapsvfphrcnfrx44w2nskgls2juwitibvqctk2plvhqd.onion/)

![tor11](https://github.com/PanosArvan/Information-Security/assets/145275148/9ce0e04f-9c0c-4186-a77c-ce703a32aaeb)

And this one about technology:

[Tech Learning Collective](http://lpiyu33yusoalp5kh3f4hak2so2sjjvjw5ykyvu2dulzosgvuffq6sad.onion/)

Hacking and security conferences that also include forums:

[InfoCon](http://w27irt6ldaydjoacyovepuzlethuoypazhhbot6tljuywy52emetn7qd.onion/)

![tor13](https://github.com/PanosArvan/Information-Security/assets/145275148/98908437-1035-4366-b5ba-dd6d9a849d03)

[DefCon](http://g7ejphhubv5idbbu3hb3wawrs5adw7tkx7yjabnf65xtzztgg4hcsqqd.onion/)

![tor12](https://github.com/PanosArvan/Information-Security/assets/145275148/853a5487-51bb-429e-9976-0fa164810fd6)
