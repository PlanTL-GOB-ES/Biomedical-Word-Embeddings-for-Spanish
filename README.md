# Biomedical Word Embeddings for Spanish: Development and Evaluation (v3.0)

## Digital Object Identifier (DOI)

Files:
- Paper: https://arxiv.org/abs/2102.12843
- Biomedical Word Embeddings: https://doi.org/10.5281/zenodo.4543235
- Biomedical Sub-word Embeddings: http://doi.org/10.5281/zenodo.4557459
- Clinical Word Embeddings: http://doi.org/10.5281/zenodo.4552042
- Clinical Sub-word Embeddings: http://doi.org/10.5281/zenodo.4555598

## Evaluation

We replicated the extrinsic evaluation from the paper [Medical word embeddings for Spanish: Development and evaluation](https://www.aclweb.org/anthology/W19-1916.pdf).

<!-- Results in HTML -->
<table class="tg">
  <tr>
    <th class="tg-0pky" colspan="3"></th>
    <th class="tg-7btt" colspan="2">Cased</th>
    <th class="tg-7btt" colspan="2">Uncased</th>
  </tr>
  <tr>
    <th class="tg-fymr">Version</th>
    <th class="tg-fymr">Method</th>
    <th class="tg-fymr">Corpora</th>
    <th class="tg-fymr">Validation</th>
    <th class="tg-fymr">Test</th>
    <th class="tg-fymr">Validation</th>
    <th class="tg-fymr">Test</th>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="3">v1.0</td>
    <td class="tg-0pky" rowspan="3">Skip-gram</td>
    <td class="tg-0pky">Wiki</td>
    <td class="tg-0pky">88.55</td>
    <td class="tg-0pky">87.78</td>
    <td class="tg-0pky">-</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO</td>
    <td class="tg-0pky">89.47</td>
    <td class="tg-0pky">87.31</td>
    <td class="tg-0pky">-</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO+Wiki</td>
    <td class="tg-0pky">89.42</td>
    <td class="tg-0pky">88.17</td>
    <td class="tg-0pky">-</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="6">v2.0</td>
    <td class="tg-0pky" rowspan="3">CBOW</td>
    <td class="tg-0pky">Wiki</td>
    <td class="tg-0pky">86.55</td>
    <td class="tg-0pky">85.46</td>
    <td class="tg-0pky">86.70</td>
    <td class="tg-0pky">86.34</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO</td>
    <td class="tg-0pky">88.11</td>
    <td class="tg-0pky">87.75</td>
    <td class="tg-0pky">86.99</td>
    <td class="tg-0pky">87.58</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO+Wiki</td>
    <td class="tg-0pky">88.68</td>
    <td class="tg-0pky">86.58</td>
    <td class="tg-0pky">86.65</td>
    <td class="tg-0pky">85.27</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="3">Skip-gram</td>
    <td class="tg-0pky">Wiki</td>
    <td class="tg-0pky">88.82</td>
    <td class="tg-0pky">87.16</td>
    <td class="tg-0pky">88.31</td>
    <td class="tg-0pky">87.43</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO</td>
    <td class="tg-0pky">89.66</td>
    <td class="tg-0pky">88.77</td>
    <td class="tg-0pky">89.57</td>
    <td class="tg-0pky">89.61</td>
  </tr>
  <tr>
    <td class="tg-0pky">SciELO+Wiki</td>
    <td class="tg-0pky">88.76</td>
    <td class="tg-0pky">88.64</td>
    <td class="tg-0pky">89.82</td>
    <td class="tg-fymr">88.28</td>
  </tr>
  <tr>
    <td class="tg-0pky" rowspan="2">v3.0</td>
    <td class="tg-0pky">CBOW</td>
    <td class="tg-0pky" rowspan="2">Bio-Corpus</td>
    <td class="tg-0pky">88.92</td>
    <td class="tg-0pky">89.12</td>
    <td class="tg-0pky">88.86</td>
    <td class="tg-0pky">88.41</td>
  </tr>
  <tr>
    <td class="tg-0pky">Skip-gram</td>
    <td class="tg-0pky">90.91</td>
    <td class="tg-0pky"><b>89.40</b></td>
    <td class="tg-0pky">89.97</td>
    <td class="tg-0pky"><b>89.66</b></td>
  </tr>
</table>

## Citing
```
@misc{temu2021spanish,
      title={Spanish Biomedical and Clinical Language Embeddings}, 
      author={Asier Gutiérrez-Fandiño and Jordi Armengol-Estapé and Casimiro Pio Carrino and Ona De Gibert and Aitor Gonzalez-Agirre and Marta Villegas},
      year={2021},
      eprint={2102.12843},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

Copyright (c) 2021 Secretaría de Estado de Digitalización e Inteligencia Artificial (SEDIA)


## Disclaimer

The models published in this repository are intended for a generalist purpose and are available to third parties. These models may have bias and/or any other undesirable distortions.

When third parties, deploy or provide systems and/or services to other parties using any of these models (or using systems based on these models) or become users of the models, they should note that it is their responsibility to mitigate the risks arising from their use and, in any event, to comply with applicable regulations, including regulations regarding the use of artificial intelligence.

In no event shall the owner of the models (SEDIA – State Secretariat for digitalization and artificial intelligence) nor the creator (BSC – Barcelona Supercomputing Center) be liable for any results arising from the use made by third parties of these models.


Los modelos publicados en este repositorio tienen una finalidad generalista y están a disposición de terceros. Estos modelos pueden tener sesgos y/u otro tipo de distorsiones indeseables.

Cuando terceros desplieguen o proporcionen sistemas y/o servicios a otras partes usando alguno de estos modelos (o utilizando sistemas basados en estos modelos) o se conviertan en usuarios de los modelos, deben tener en cuenta que es su responsabilidad mitigar los riesgos derivados de su uso y, en todo caso, cumplir con la normativa aplicable, incluyendo la normativa en materia de uso de inteligencia artificial.

En ningún caso el propietario de los modelos (SEDIA – Secretaría de Estado de Digitalización e Inteligencia Artificial) ni el creador (BSC – Barcelona Supercomputing Center) serán responsables de los resultados derivados del uso que hagan terceros de estos modelos.
