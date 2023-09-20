# Semantic Annotations for the RICO dataset

**Contact -** srinivasksun@google.com

## Overview

The **RICO Semantics** dataset consists of around 500k human annotations on the
[RICO](https://interactionmining.org/rico) dataset identifying various icons
based on their shapes and semantics, and associations between selected general
UI elements (like icons, form fields, radio buttons, text inputs) and their text
labels. The annotations also include human annotated bounding boxes which are
more accurate and have a greater coverage of UI elements than using bounding
boxes from the view hierarchy. This dataset enables building models for
understanding the contents of user interfaces and hence can act as a stepping
stone for improving the accessibility of user interfaces.

**The datasets are provided "AS IS" without any warranty, express or implied.
Google disclaims all liability for any damages, direct or indirect, resulting
from the use of this dataset.**

## Important Links

*   [Paper - Towards Better Semantic Understanding of Mobile Interfaces](https://arxiv.org/abs/2210.02663)
*   [Data processing and modeling code](https://github.com/google-research/google-research/tree/master/rico_semantics)
*   [RICO dataset](https://interactionmining.org/rico) and
    [paper](http://ranjithakumar.net/resources/rico.pdf).

## Data

The RICO Semantics datasets augments the RICO dataset with high-quality human
annotations aimed at increasing the semantic understanding of various UI
elements. We provide annotations for 3 different tasks: `Icon Shape` consisting
of icon annotations based on their shape, `Icon Semantics` consists of icon
annotaitons based on their functionality and `Label Association` identifying
various UI elements and associating these UI elements with their text labels.
Compared to previous approaches which rely on bounding boxes from the View
Hierarchy, we release bounding boxes manually annotated by human raters. We
observe that this results in a significantly higher coverage for UI elements. In
total, the annotations include `350k` annotations for `Icon Shape`, `78k`
annotations for `Icon Semantics` and `66k` UI elements with associated text
labels. Please refer to [our paper] for more details.

### Annotation Representation

The annotations are released as JSON files. Each entry in the JSON file contains
the ID of the raw RICO data in the field: `screen_id`. All the annotations are
present in the field `screen_elements`. This field contains a list of
annotations for the UI elements present. The annotation data includes the
relative coordinates (normalized to the range \[0, 1\]) of the bounding box for
each label and the class associated with the bounding box. The screen elements
are not in any particular order. The annotations are also split into `train`,
`val` and `test` splits. These splits correspond to the numbers reported in
**Section 4** of our paper.

## License

The RICO Semantics dataset is released under
[**CC BY-SA 4.0**](https://creativecommons.org/licenses/by-sa/4.0/) license. For
the full license, see [LICENSE](LICENSE). Please cite the following paper if you
use the dataset in your work:

```shell
@article{https://doi.org/10.48550/arxiv.2210.02663,
  author    = {Srinivas Sunkara and
               Maria Wang and
               Lijuan Liu and
               Gilles Baechler and
               Yu-Chung Hsiao and
               Jindong Chen and
               Abhanshu Sharma and
               James Stout},
  title     = {Towards Better Semantic Understanding of Mobile Interfaces},
  journal   = {CoRR},
  volume    = {abs/2210.02663},
  year      = {2022},
  url       = {https://arxiv.org/abs/2210.02663},
  eprinttype = {arXiv},
  eprint    = {2210.02663},
  timestamp = {Thu, 06 Oct 2022 15:00:01 +0100},
}
```

## Dataset Metadata

The following table is necessary for this dataset to be indexed by search
engines such as <a href="https://g.co/datasetsearch">Google Dataset Search</a>.
<div itemscope itemtype="http://schema.org/Dataset">
<table>
  <tr>
    <th>property</th>
    <th>value</th>
  </tr>
  <tr>
    <td>name</td>
    <td><code itemprop="name">Rico Semantics dataset</code></td>
  </tr>
  <tr>
    <td>alternateName</td>
    <td><code itemprop="alternateName">Rico Semantic Annotations dataset</code></td>
  </tr>
  <tr>
    <td>url</td>
    <td><code itemprop="url">https://github.com/google-research-datasets/rico-semantics</code></td>
  </tr>
  <tr>
    <td>description</td>
    <td><code itemprop="description">The dataset adds annotations to the RICO dataset to improve the semantic understanding of UIs. This dataset consists of human annotated bounding boxes and class labels for <b>3 tasks:</b> <i>Icon Shape</i>, <i>Icon Semantics</i> and <i>Label Association</i>.</code></td>
  </tr>
  <tr>
    <td>provider</td>
    <td>
      <div itemscope itemtype="http://schema.org/Organization" itemprop="provider">
        <table>
          <tr>
            <th>property</th>
            <th>value</th>
          </tr>
          <tr>
            <td>name</td>
            <td><code itemprop="name">Google</code></td>
          </tr>
          <tr>
            <td>sameAs</td>
            <td><code itemprop="sameAs">https://en.wikipedia.org/wiki/Google</code></td>
          </tr>
        </table>
      </div>
    </td>
  </tr>
  <tr>
    <td>citation</td>
    <td><code itemprop="citation">https://identifiers.org/arxiv:2201.12409</code></td>
  </tr>
</table>
</div>
