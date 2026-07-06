![[Pasted image 20260706213314.png]]
**Link:** [Aurora Linux](https://getaurora.dev/en/)

I am in love with the idea of *immutable distros* since I used [[Steam Deck]]. A linux that runs the games without issues and does not croak when receiving an update? Sign me up!

I mean... if you are not using an Asus ROG Laptop...
## Good Things
- The installation is smooth. I also liked the Flatpak aspect of things - as you don't mess around with the "Core" system you install everything via Flatpak.
- Bazaar is awesome. I don't know if it is an Aurora thing by default but I've seen and installed some new programs I haven't heard before and was pleasantly surprised. It makes a good showcase of the Linux software ecosystem and how far it had come
- KDE. The eyecandy is just beautiful.

## Bad things
- System stability. My Asus ROG died for no reason. I know I could revert whatever change to the previous state but it bothered me
- I know it is a me thing but under Linux I cannot undervolt my system. Asus ROG just LOVES to burn itself to bits when left alone to its devices. Some turbo boost disabling here, some undervolt there and you can have Cyberpunk 2027 running in low 70 degrees with no loss in graphical fidelity. 
- Flatpak. Because everything is installed in a non touchy way, some apps' functionalities are crippled or have to be handled in a more verbose way. I did not like it. Also you are prisoned to the Bazaar and/or Brew ecosystem. Truth be told, all of my apps were there, so I am not grumbling that much but I could have.

## Overall
I can see myself using this distro if I hadn't owned an Asus ROG G14. Also it is a testament to see how far the Linux come since the bad old days of 2000s. Now it is going toe to toe with Mac - after W11, the less we talk about Windows, the better.

# Troubleshooting
## `UNABLE_TO_GET_ISSUER_CERT_LOCALLY` Error
`brew install node` command does not point to the ca certificates - resulting in plugin install errors. 

To fix it we run this command:

`npm config set cafile /etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem`

## Failed to Emit ogimage
This didn't happen on Windows but Linux yelled at me on 

	npx quartz build --serve

With the og-image plugin. Solution **disable it** from `quartz.config.yaml`
## Tags
#linux #unsorted 