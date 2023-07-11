# my-lit-llama
How to run lit-llama

## Commands:

### Clone the repo:

```
git clone https://github.com/Lightning-AI/lit-llama
cd lit-llama
```
### Install the requirements:

```
pip install -r requirements.txt
```

### Download llama weights data:

```
python scripts/download.py --repo_id openlm-research/open_llama_7b --local_dir checkpoints/open-llama/7B
```

## Customize paths

The project is setup to use specific paths to read the original weights and save checkpoints etc.

For all scripts, you can run

```shell
python script.py -h
```

to get a list of available options. For instance, here's how you would modify the checkpoint dir:

```shell
python scripts/convert_checkpoint.py --checkpoint_dir "data/checkpoints/foo"
```

Note that this change will need to be passed along to subsequent steps, for example:

```shell
python generate.py \
  --checkpoint_path "data/checkpoints/foo/7B/lit-llama.pth" \
  --tokenizer_path "data/checkpoints/foo/tokenizer.model"
```

and

```shell
python quantize/gptq.py \
  --checkpoint_path "data/checkpoints/foo/7B/lit-llama.pth" \
  --tokenizer_path "data/checkpoints/foo/tokenizer.model"
```

To avoid this, you can use symbolic links to create shortcuts and avoid passing different paths.


### Install SciPy
```
 pip install scipy 

```

### To execute the chatbot in 8bit mode:

```
python generate.py --quantize llm.int8 --prompt "Hello, my name is"
```
### Create links

```
ln -s /home/mostafa/programming/models/llama/pyllama_data/7B/consolidated.00.pth checkpoints/lit-llama/7B/lit-llama.pth
```
```
ln -s /home/mostafa/programming/models/llama/pyllama_data/tokenizer.model checkpoints/lit-llama/tokenizer.model
```
