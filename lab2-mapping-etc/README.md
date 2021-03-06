# Lab 2

[Boot a Jetstream instance](../lab1-jetstream/boot.md)

## Look at some FASTQ data

1. In a Web browser, go to [the ENA record for SRX1317384](https://www.ebi.ac.uk/ena/data/view/SRX1317384)

2. Copy the url for `Fastq files (ftp)`, `File 1`.

3. In your terminal, execute `curl -O ` and then paste in the URL.

4. Wait for it to download.

5. Run

        gunzip -c SRR2584857_1.fastq.gz | head
        
   Marvel at the FASTQ!

6. Install [FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/):

First install the prerequisites:
```
sudo apt-get -y install openjdk-8-jre libcommons-math3-java libjbzip2-java
```

and then install fastqc:

```
cd ~/
wget https://launchpad.net/ubuntu/+archive/primary/+files/fastqc_0.11.5+dfsg-3_all.deb && \
sudo apt-get install -f && \
sudo dpkg -i fastqc_0.11.5+dfsg-3_all.deb
```

7. Run FastQC:

        fastqc SRR2584857_1.fastq.gz

8. If you know how to download files from a remote host, do so for the file `SRR2584857_1_fastqc.zip`; otherwise you can download the resulting file by [clicking on this link](https://github.com/ngs-docs/2018-ggg201b/raw/master/lab2-mapping-etc/SRR2584857_1_fastqc.zip).  If you open this file, you will see `fastqc_report.html`; double-click on that to open it in a browser.  This is a quality report on that file.

There's a [nice tutorial](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/) on the FastQC web site for those who are interested in more.

## REMEMBER TO DELETE YOUR JETSTREAM INSTANCE.
