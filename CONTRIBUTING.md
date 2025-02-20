## Development Setup

```
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt

playwright install
```

## Web scrapper research (02/20/2025)
Tried scrapegraph-ai, but soon hit error: [KeyError: 'Input to PromptTemplate is missing variables](https://github.com/ScrapeGraphAI/Scrapegraph-ai/issues/926)
Exploring Scrapy and created a [request](https://github.com/scrapy/scrapy/issues/6687) to integrate with AI providers
## Front end mock (02/19/2025)

See [Vercel mock](https://v0-female-scientist-profiles-g90dwq.vercel.app/) (It's a mock, it hasn't connect to the real database yet)
The front has few features:

1. Display random female scientists profile
2. Search female scientists by name, subject, affiliated institutions, keywords

## System diagram (02/18/2025)

![Alt text](system_diagram.png?raw=true)

## Preserve female scientists history (02/18/2025)

In light of the recent event that female scientists were removed from their organization's websites, I'm considering a way to preserve female scientists' history.

Technical Proposal:
Currently, the website is controlled by a centralized entity, e.g. university, NASA...which may delete the content due to pressure. I'm thinking using blockchain to decentralize the ownership. Once the data is on the chain, it cannot be deleted arbitrarily. Anyone willing, can build a front end to render and display the data, but none of them can manipulate/delete the data. In this way, we again decentralize the front end. Even if 1 front end website being "cracked down", we can easily build more.

I initiated a repository to start my work: https://github.com/ctseng777/HypatiaofAlexandria

Challenges:

1. How to guarantee the data written to the chain is authentic? Although I could help validating the truth, it's not scalable and I wouldn't feel comfortable being the "authority" for long term. I think, I could make the software regularly scan major websites, e.g. universities, NASA... and detect addition and deletion; or grant temp writing permission to female scientists using their email affiliation.
2. Funding: Every writing to the chain can cost a bit gas fee. Although I could foot the cost in the beginning. I will need to raise funding once scaled up.
