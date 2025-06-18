Provided code contains methods of splitting the text according to the LLM parameters so that the LLM could summarize
the document without truncating the length of the original text

How to run the code:
1) Install Python and IDE (PyCharm, Visual Studio Code, etc)
2) Install libraries
   pip install --upgrade pip setuptools wheel
   pip install numpy
   pip install torch
   pip install transformers
   pip install nltk
   pip install protobuf
   pip install streamlit
   pip install hf_xet
   pip install cmake
   pip install sentencepeice
   In case errors occur follow the instructions of pip
3) Run the following codes to download the models locally before using them
   
   from transformers import PegasusTokenizer, PegasusForConditionalGeneration

   model_name = "google/pegasus-cnn_dailymail"
   
   model = PegasusForConditionalGeneration.from_pretrained(model_name)
   tokenizer = PegasusTokenizer.from_pretrained(model_name)
   
   --------------------------------------------------------

   from transformers import BartTokenizer, BartForConditionalGeneration

   model_name = "facebook/bart-large-cnn"
   
   model = BartForConditionalGeneration.from_pretrained(model_name)
   tokenizer = BartTokenizer.from_pretrained(model_name)

   ---------------------------------------------------------

   from transformers import T5Tokenizer, T5ForConditionalGeneration

   model_name = "t5-base"

   model = T5ForConditionalGeneration.from_pretrained(model_name)
   tokenizer = T5Tokenizer.from_pretrained(model_name)

5) Copy the code from the file "code" in this repository and paste to your IDE
6) Execute in python terminal or in cmd: streamlit run "E:\Path\to\file\python_file.py"
That's it. Follow the isntructions on the web page. Don't forget to press Ctrl+Enter after you have entered the text manually.
If there is a file pinned, the model will take the file. Otherwise a manually entered text will be chosen
