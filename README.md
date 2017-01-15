# Blast

This is a singularity image to deploy blast.

This will produce a Singularity image (suitable for running in a cluster environment) using [https://hub.docker.com/r/broadinstitute/picard/](https://hub.docker.com/r/broadinstitute/picard/). We do this by way of a bootstrap file for the Docker image.


## 1. Install Singularity

Instructions can be found on the [singularity site](https://singularityware.github.io).


## 2. Bootstrap the image


    sudo singularity create --size 4000 blast.img
    sudo singularity bootstrap blast.img Singularity


## 3. Run commands

How to access the blast runtime executables?


       ./blast.img

	This container provides the following executables:
	2to3		   genbrk		 python-config
	activate	   gencfu		 python2
	blast_formatter    gencnval		 python2.7
	blastdb_aliastool  gendict		 rpsblast
	blastdbcheck	   gene_info_reader	 rpstblastn
	blastdbcmd	   genrb		 seedtop
	blastdbcp	   icu-config		 segmasker
	blastn		   icuinfo		 seqdb_demo
	blastp		   idle			 seqdb_perf
	blastx		   legacy_blast.pl	 smtpd.py
	c_rehash	   makeblastdb		 sqlite3
	conda		   makeconv		 tblastn
	conda-env	   makembindex		 tblastx
	convert2blastmask  makeprofiledb	 tclsh8.5
	datatool	   openssl		 test_pcre
	deactivate	   pip			 uconv
	deltablast	   pkgdata		 update_blastdb.pl
	derb		   project_tree_builder  wheel
	dustmasker	   psiblast		 windowmasker
	easy_install	   pydoc		 windowmasker_2.2.22_adapter.py
	easy_install-2.7   python		 wish8.5

	Example usage: blast.img blastn [args] [options]



      ./blast.img blastn
