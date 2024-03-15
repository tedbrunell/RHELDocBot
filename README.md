# Red Hat Enterprise Linux Documentation Chat Bot (RHELDocBot)
The RHELDocBot is a simple Large Language Model with Retrieval Augemnted Generation (LLM RAG) Jupyter Notebook that is meant to demoonstrate the usefulness of this technology for anyone that has a document or policy library that is often searched of information.  The RHEL DocBot ingests those documents and makes them available for question and answer retreival.

## Documents that were used
As a Red Hat employee (and big fan of RHEL) I dedcided to use 7 different documents for RHEL 9 that are all publicly available for this demo.
- Performing a standard RHEL 9 installation
- Performing an advanced RHEL 9 installation
- Security hardening for RHEL 9
- Composing a customized RHEL system image
- Upgrading from RHEL 8 to RHEL 9

## How to use
1.  Download and import the included notebook into Jupyter.
    **Note:** The playbook assumes that you have Ollama running somewhere and that it can be access over port 11434.
2.  Change the question at the bottom of the notebook.
3.  Run all of the code in the notebook.  The first time that the notebook is run, it will download the documents, chunk them and store the processed chunks into a chroma vector database.  Once the database is created, subsequent runs of the notebook will be much faster.
4.  The initial question will be answered when the notebook is done executing.  Change the question and run just the last block again (and again and again).

The answer should include references to will take you to the doccumentation that was used to generate the answer.

LLMs are not perfect and sometimes you will receive quesstions taht are wrong or incomplete.  Feel free to provide input if anything can be improved to make this more useful or accurate!
