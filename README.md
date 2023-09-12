<h1>Fix "snd_hda_intel" audio modules in linux</h1>
<h2>Check audio card:</h2>
<p>Terminal command:</p>
<p>First command: >>>aplay -l<br>result: "no soundcard found..."</p>
<p>Next command:  >>>lspci -v | grep -A7 -i "audio"<br>See at end line:"Kernel modules: snd_hda_intel, snd_sof_pci_intel_cnl"</p>
<h2>Fix bug:</h2>
<h4>Method 1:</h4>
  <p>1.Enter the default grub file with sudo nano /etc/default/grub<br>
2.Change GRUB_CMDLINE_LINUX_DEFAULT="..." to GRUB_CMDLINE_LINUX_DEFAULT="... snd_hda_intel.dmic_detect=0"<br>
3.Apply the changes with sudo update-grub<br>
4.Reboot</p>
<h4>Method 2:</h4>
<p>add "options snd-hda-intel dmic_detect=0" at the and "/etc/modprobe.d/alsa-base.conf" file<br>then "reboot" device! or use this commend: >>>pulseaudio -k && sudo alsa force-reload
</p>
