# Jinja template for Ocean C2D

> Note: work-in-progress

A template for easily converting jupyter notebooks to Ocean Protocol C2D script. Use tags to specify different parts of your jupyter notebooks.

## 🏗 Initial Setup

### Set up environment
```
#clone repo
git clone https://github.com/AlgoveraAI/same-project.git
cd same-project

#create a virtual environment
python3 -m venv venv

#activate env
source venv/bin/activate

#Install the dependencies
pip install -e .
pip install jupyter
```

### Guide to using the template
Open up a jupyter notebook. This is where you will do all your data analysis and model development. Make sure to write a comment at the start of each cell (this is necessary otherwise the template will generate incorrectly indented code).

When you are done developing locally and want to publish to ocean, you will need to tag specific cells of your notebook to be read by the template. To do this click *View/Cell Toolbar/Tags*.
Tag the cells where you did your data preparation with "input" and the cells with your model and training loop "train".

When you're ready execute the following command in your terminal:
```
jupyter nbconvert path_to_notebook --to python --template=./sameproject/ops/python_ocean
```

Check that the generated script has no syntax errors.

See `dcgan.ipynb` and `dcgan.py` for more details and reach out if you run into issues.

## Algovera

Algovera is a community of individuals working to facilitate and accelerate the development of decentralised AI products and research.

[Website](https://www.algovera.ai/) | [Notion](https://algovera.notion.site/) | [Discord](https://discord.gg/e65RuHSDS5) | [Calendar](https://calendar.google.com/calendar/embed?src=c_4qajdfj4imie9cpnkbvkrc7ri4%40group.calendar.google.com) | [Twitter](https://twitter.com/AlgoveraAI) | [YouTube](https://www.youtube.com/channel/UC2A5iUpP6k52ZZmC8LFj1IA) |

