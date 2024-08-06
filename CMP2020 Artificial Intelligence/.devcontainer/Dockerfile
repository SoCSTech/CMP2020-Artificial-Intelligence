FROM ubuntu:latest

RUN apt upgrade && apt update

RUN apt -y install python3 swi-prolog cmake curl build-essential git-all
RUN apt -y install python3-pip

RUN curl -d "action=AttachFile&do=get&target=fast-downward-23.06.tar.gz" -o fast-downward-23.06.tar.gz https://www.fast-downward.org/Releases/23.06 &&\
tar -xvzf fast-downward-23.06.tar.gz &&\
cd fast-downward-23.06 &&\
./build.py

RUN pip install --break-system-packages mesa
RUN pip install --break-system-packages scikit-learn scipy matplotlib numpy seaborn
RUN pip install --break-system-packages ipykernel