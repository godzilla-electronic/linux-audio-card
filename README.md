<h1>Fix "snd_hda_intel" audio modules in linux</h1>
<h2>Check audio card:</h2>
<p>Terminal command:</p>
<p>First command: >>>aplay -l<br>result: "no soundcard found..."</p>
<p>Next command:  >>>lspci -v | grep -A7 -i "audio"<br>See at end line:"Kernel modules: snd_hda_intel, snd_sof_pci_intel_cnl"</p>

