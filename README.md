
Please cite the following if you use this code.
```
@inproceedings{reboud2021,
  title={Events Zero-Shot Classification for Character-Centric Video Summarization },
  author={Reboud, Alison and Harrando, Ismail and  Lisena, Pasquale and Troncy, Rapha{\"e}l},
  booktitle={International Workshop on Video Retrieval Evaluation},
  year={2021}
}
```

# trecvid-vsum
Steps to reproduce the final MeMAD approach for the TRECVID VSUM 2021 task
![Model architecture](vsum.png)

1) Using [`shots_transcripts_alignment.ipynb`](./transcripts/shots_transcripts_alignment.ipynb), align the transcript content with the shot ID i.e. given the transcript files and [master shot reference table](./facerec_segment/eastenders.masterShotReferenceTable.txt), a CSV containing what was said in each shot (based on the transcript and shot boundaries) is produced ([shot-aligned_transcripts.csv](./transcripts/shot-aligned_transcripts.csv)).
2) Face recognition: we select the shots displaying any of the the three characters of interests, keeping only those detection having a confidence scoregreater than 0.5 ([`facerec_query_characters.csv`](./facerec_segment/facerec_query_characters.csv)).
In order to do so, we performed face recognition using our  [Face Recognition Service](https://github.com/D2KLab/FaceRec). The results can be found under [facerec_out](./facerec_out) (2.challenge_people). We use [`facerec_output_preprocessing.ipynb`](./facerec_segmentation/facerec_output_preprocessing.ipynb) to transform the JSON output into a CSV files with timestamps for each detection, then  [`facerec_segmentation.ipynb`](./facerec_segmentation/facerec_segmentation.ipynb) to align the detections with the shot IDs.
Note : this folder also includes facerec results for a larger pool of EastEnders characters, as well as results of facerec with different thresholds of confidence, which experimented with but did not use in the final submission.
3) Perform Zero Shot Classification with event labels
4) Generate the shot candidate shots for the summary with [`submission_generation.ipynb`](./submission/submission_generation.ipynb). This is done by first concatenating the output of the previous steps (i.e. aligning coreference-resolved transcripts and facerec output with the [master shot reference table](./facerec_segment/eastenders.masterShotReferenceTable.txt)), so that the content of each shot is aligned (time-wise) with the shot IDs. The next step is to compute the similarity between each shot content and the synopses sentences as described in the paper. The N shots (N varying per run) with the higher similarity scores are picked and written into XML files ([`submissions`](./submission/xml)).




