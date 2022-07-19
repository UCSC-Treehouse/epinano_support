# epinano_support

The dockerfile creates a docker that runs [EpiNano](https://github.com/novoalab/EpiNano). It is a revised version of the Dockerfile in the EpiNano repository. 

After building the docker, it is run interactively. e.g. 

```
docker run -it --rm \
-v /mnt/:/mnt/ \
--entrypoint=/bin/bash \
hbeale/tree_epinano:1

```

and EpiNano is called with a command like

```
python3 /usr/local/bin/EpiNano/Epinano_Variants.py -R $ref_fa -b $bam -n 6 -T t -s /usr/local/bin/EpiNano/misc/sam2tsv.jar
```
