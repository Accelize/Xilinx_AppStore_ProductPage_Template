# Xilinx App Store - Product Page Creation Process
A Xilinx App Store Product Page is generated automatically from two kind of input files: 

+ A **Definition File**
+ A set of **Instructions Files**

## The Definition File
A Yaml file containing business and marketing information about your application

You can find the template in [template/vendor-name_app-name/vendor-name_app-name.yaml](template/vendor-name_app-name/vendor-name_app-name.yaml)

### How-to fill the Definition File:
1. Replace strings "vendor-name" and "app-name" 
  1.1 In the file names
  1.2 In paths 
  1.3 In content of this file

2. Fill the "Application Summary" section
  2.1 Replace "TODO" strings

3. Fill the "Deployment Options" section
  3.1 Replace "TODO" strings

4. Fill the "Running the Application" section
  4.1 Replace the content between '"' by Markdown text 
  
5. Do not edit or change the following sections:
  5.1 "Try or Buy CTA URLs"
  5.2 "Test Drive"

6. Provide assets to your Accelize FAE:
  6.1 Logo picture, Embeded Video, Solution Brief, User Guide, ...


## The Instruction Files
Markdown files describing the step-by-step instruction to run the docker application (one file per target environment)

You can find two template here: 
+ Alveo:  [template/vendor-name_app-name/instructions/alveo_u200.md](template/vendor-name_app-name/instructions/alveo_u200.md)
+ AWS F1: [template/vendor-name_app-name/instructions/aws_f1.md](template/vendor-name_app-name/instructions/aws_f1.md)

### How-to fill the Instruction Files:
Use Markdown in these files.
> Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.

Read More: [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)

&#x26a0;&#xfe0f; You can't use Heading level one (#). The highest level usable is level 2 (##)
&#x26a0;&#xfe0f; You can only embed one picture per section. This picture will be place on the right side of Product Page.

## Example files
You can find example Definition and Instruction file here:
[examples/xilinx_vitisai](examples/xilinx_vitisai)


## Product Page Definition and instructions files Delivery
Once updated, please share the Product Page Definition and instructions files within a .zip or .tar.gz/.tgz archive with following hierarchy:

&#x1F4E6; vendor-name_app-name.tar.gz
  + &#x1F4C1; vendor-name_app-name
    + &#x1F4C1; assets
      + &#x1F5BC; logo.png
      + &#x1F5BC; app_screenshot_1.png
      + &#x1F4DD; solution_brief.pdf
      + &#x1F4DD; user_guide.pdf
    + &#x1F4C1; instructions
      + &#x1F4DD; target-platform_1.md
      + &#x1F4DD; target-platform_2.md
    + &#x1F4DD; vendor-name_app-name.yaml

