# C-learning-feedback-
This is my personal learning c++ language feedback 


vector<vector<float> > gettable(string filename){
    int count=0;
    int record=0;
    string line;
    string temp;
    vector<string> out;

    vector<string> data;
    vector<vector<string> > haha;
    ifstream input(filename);

       if (input.is_open()) {
        while (getline(input, line)) {
             count++;
             if (count==1) continue;

                for(int i=0;i<line.length();i++){

                    if (line[i]!=32){
                        temp+=line[i];
                        if(line[i+1]==32||i==(line.length()-1)){
                            data.push_back(temp);
                            temp.erase();
                        }
                    }
                }
                haha.push_back(data);
                data.clear();
            //      if (count==100){
            //  input.close();
            // }
          

        }
        input.close();

       }

    vector<vector<float> > newdata;
    vector<float> tempp;


    for(int i=0;i<haha.size();i++){
        output.push_back(haha[i].back());   //out value
    }
    for(int i=0;i<haha.size();i++){
        haha[i].back()=to_string(i);
    }

    for(int i=0;i<haha.size();i++){
          for(int k=0;k<haha[0].size();k++){
             tempp.push_back(stof(haha[i][k]));
          }
        newdata.push_back(tempp);
        tempp.clear();
    }



      return newdata;

}
