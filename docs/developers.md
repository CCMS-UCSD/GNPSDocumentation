If you're a developer, computer scientist, bioinformatician, or software enthusiast and you want to contribute to GNPS, we'd love to have your support. Given security concerns of running on a shared cluster, we didn't want to fully close off the development from outside of UC San Diego, but rather have the following avenues of development to engage the community.

## Adding Functionality to Existing Workflows

This is the most straightforward process as it simply entails modifying/adding new code to existing GNPS workflows. Almost all GNPS workflows are open source and can be found on [GitHub](https://github.com/CCMS-UCSD/GNPS_Workflows). Let us know if there is a new issue or feature you want to address and we'll work together to get you up to speed, merge the code, test it on our development servers, and eventually promote it to GNPS.  

## Developing New Workflows For New Tools

This pathway is a bit more difficult as it requires writing ProteoSAFe workflow files. What we've found is likely the simplest path forward to start is reaching out once you have a single commandline tool ready along with the dependencies you need (e.g. requirements.txt, conda-environment.yml, etc.) and we can use our boiler plate workflow template to get your workflow onto our beta server. Due to security restrictions on our server, you won't be able to deploy directly, but we will be able to help you with those deployments. 

Feel free to [contact us](contact.md) to discuss what you want to get into GNPS and then we'll do the fun thing and run that tool over all public data, what the worst that could happen? 