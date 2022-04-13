# Question:
Does anyone know if ARC allocates each personal scratch (where I could temporarily process large size datasets) or not? I basically tried to use '/scratch', but it denied my permission.. or in which folder (or partitioned space) do you guys normally used when producing large size intermediate files (i.e., all the intermediate contigs for each k-mer during de-novo assembly, etc) in ARC?

# Answer
You get a subdirectory in scratch for each job, /scratch/${SLURM_JOB_ID}
