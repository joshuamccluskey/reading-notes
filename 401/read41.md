# Analytics and Text-To-Speech

## Read 341

### Joshua McCluskey


#### AWS Pinpoint
- AWS Pinpoint is basically e marketing using email, SMS, Push Notification, and In - App Messaging
- You can customize marketing based on your audience segmentation
- You can create the templates to be used for these to personalize them
- You can set campaign schedules
- You establish a journey for a set experience for your participant
- Transactional messages are on-demand messages for specific receivers
- You can set up analytics to see how people are interacting 


#### Amazon Polly

- Takes text and converts it into speech
- Neural Text-to-Speech NTTS
- Used for readers, education games and accessibility 
- You can have accented bilingual voices
- Neural voices are supporte din certain regions

````Java
//Get Lexicaon sample code
package com.amazonaws.polly.samples;
 
import com.amazonaws.services.polly.AmazonPolly;
import com.amazonaws.services.polly.AmazonPollyClientBuilder;
import com.amazonaws.services.polly.model.GetLexiconRequest;
import com.amazonaws.services.polly.model.GetLexiconResult;
 
public class GetLexiconSample {
    private String LEXICON_NAME = "SampleLexicon";
 
    AmazonPolly client = AmazonPollyClientBuilder.defaultClient();
 
    public void getLexicon() {
        GetLexiconRequest getLexiconRequest = new GetLexiconRequest().withName(LEXICON_NAME);
 
        try {
            GetLexiconResult getLexiconResult = client.getLexicon(getLexiconRequest);
            System.out.println("Lexicon: " + getLexiconResult.getLexicon());
        } catch (Exception e) {
            System.err.println("Exception caught: " + e);
        }
    }
}
````
- [credit](https://docs.aws.amazon.com/polly/latest/dg/what-is.html)

#### Things I want to learn more about

#### Reading

- [AWS Pinpoint](https://aws.amazon.com/pinpoint/features/?nc=sn&loc=2)
- [Amazon Polly](https://docs.aws.amazon.com/polly/latest/dg/what-is.html)


[<=== Back](../README.md)