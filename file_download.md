### Download the necessary files

__Adapting for MCF7__ 

Galaxy:
https://usegalaxy.eu/datasets/4838ba20a6d86765d1685afe6504d674/preview
#Use galaxy to visualize downloaded datasets in a UI friendly environment.

<br>
ENCODE View:

https://www.encodeproject.org/search/?searchTerm=mcf7&type=Dataset  
#Overall MCF7 sample datasets  

https://www.encodeproject.org/reference-epigenomes/ENCSR247DVY/  
#MCF7 Reference - containing multiple bioassays.  

https://www.encodeproject.org/annotations/ENCSR074VNQ/  
#MCF7 cCRE annotation file - checked on Galaxy and is same format to one used in  tutorial.

<br>
Use rsync to transport directory of files to remote server, 
<br>  
<font color="purple"> Example: </font>
<br>
rsync MCF7_IDR_thresholded_peaks.bed meluxina:/project/home/p200469/get_BIO1018/
<br>
rsync peak_counts.txt meluxina:/project/home/p200469/get_BIO1018/  

<br>
<br>  
or,  

<br>

curl directly from the terminal:  
curl -o MCF7_IDR_thresholded_peaks.bed.gz https://www.encodeproject.org/files/ENCFF882OVP/@@download/ENCFF882OVP.bed.gz  
curl -o cCRE_hg38.bed.gz https://www.encodeproject.org/files/ENCFF377XIH/@@download/ENCFF377XIH.bed.gz  

<br>
-O: Saves the file with its original name.  
<br>
-o: Allows you to specify a custom name for the downloaded file.

<br>
<br>

<font color="red"> Error:</font>
using curl causes the file to download as a HTML file rather than a real, valid gzip file.  

<font color='green'> Solution:</font> 
<br>
Use wget instead:  
wget https://www.encodeproject.org/files/ENCFF377XIH/@@download/ENCFF377XIH.bed.gz  
wget https://www.encodeproject.org/files/ENCFF882OVP/@@download/ENCFF882OVP.bed.gz - IDR Threshold Peaks  
wget https://www.encodeproject.org/files/ENCFF607OSL/@@download/ENCFF607OSL.bam - ATAC-Seq BAM File  
  

> Just an example, explore other files to increase size and power of data.
