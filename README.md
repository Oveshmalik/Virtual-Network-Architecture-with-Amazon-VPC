
<body>

<h1>Building a Modular and Scalable Virtual Network Architecture with Amazon VPC</h1>

<p>Welcome to the repository for my groundbreaking project on building a modular and scalable virtual network architecture using Amazon Virtual Private Cloud (VPC). This project, undertaken during my first semester of the <b>Cybersecurity and Threat Management program at Seneca College</b>, delves deep into the intricacies of leveraging Amazon VPC to create a robust and flexible network infrastructure tailored to modern cloud computing needs.</p>

<h2>What's Inside?</h2>

<p>In this repository, you'll find comprehensive documentation detailing our approach, methodologies, and the technical insights gained throughout the project. From initial conceptualization to implementation strategies and best practices, I've meticulously documented every aspect to provide a comprehensive resource for anyone interested in harnessing the power of Amazon VPC for their network architecture needs.</p>

<h3>Key Features:</h3>
<ul>
    <li><strong>Modularity:</strong> Explore how we designed our network architecture to be modular, allowing for easy expansion and customization.</li>
    <li><strong>Scalability:</strong> Learn about the scalability principles employed to ensure our network can adapt to growing demands seamlessly.</li>
    <li><strong>Flexibility:</strong> Discover the flexibility offered by Amazon VPC, empowering users to tailor their network setup to specific requirements.</li>
    <li><strong>Best Practices:</strong> Gain valuable insights into industry best practices for designing and managing virtual network architectures.</li>
</ul>

<h2>Let's Get Started</h2>

<p>
    <img src="/Images/vpc-architecture_diagram.png" alt="Description of the image" width="1000">    
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">The Above Virtual Private Cloud Architecture will be created in 1 region and will span in 4 different availability zones for high availability and fault tolerance purpose. Each availability zone will have 4 group of Subnets. 1 public 2 private and 1 spare for future use.</span></p>
<p><span style='font-size:16px;font-family:"Calibri",sans-serif;'>The following table is a list of CIDR block for each subnet that we will be deploying in 4 different availability zones.<br>&nbsp;</span></p>
<div align="center" style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>
    <table style="border: none;border-collapse:collapse;">
        <tbody>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-right: none;border-left: none;border-image: initial;border-bottom: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">VPC</span></em></strong></p>
                </td>
                <td style="width: 131.8pt;border-top: none;border-right: none;border-left: none;border-image: initial;border-bottom: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">10.0.0.0/16</span></em></strong></p>
                </td>
                <td style="width: 142.3pt;border-top: none;border-right: none;border-left: none;border-image: initial;border-bottom: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">Availability Zone 1</span></em></strong></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">10.0.0.0/18</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">&nbsp;</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Public Subnet</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">10.0.32.0/20</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Private Subnet A</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">10.0.0.0/19</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Private Subnet B</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.48.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Spare subnet</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">10.0.56.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">Availability Zone 2</span></em></strong></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">10.0.64.0/18</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">&nbsp;</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Public Subnet</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.96.0/20</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Private Subnet A</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.64.0/19</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Private Subnet B</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.112.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Spare subnet</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.120.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">Availability Zone 3</span></em></strong></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">10.0.128.0/18</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">&nbsp;</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Public Subnet</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.160.0/20</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Private Subnet A</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.128.0/19</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Private Subnet B</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.176.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Spare subnet</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.184.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><strong><em><span style="font-size:16px;color:black;">Availability Zone 4</span></em></strong></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">10.0.192.0/18</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">&nbsp;</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Public Subnet</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.224.0/20</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Private Subnet A</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.192.0/19</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:black;">Private Subnet B</span></p>
                </td>
                <td style="width: 142.3pt;background: rgb(242, 242, 242);padding: 0in 5.4pt;height: 18.65pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.240.0/21</span></p>
                </td>
            </tr>
            <tr>
                <td style="width: 162.65pt;border-top: none;border-bottom: none;border-left: none;border-image: initial;border-right: 1pt solid rgb(127, 127, 127);background: white;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;text-align:right;line-height:normal;'><em><span style="font-size:16px;">&nbsp;</span></em></p>
                </td>
                <td style="width: 131.8pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;">Spare subnet</span></p>
                </td>
                <td style="width: 142.3pt;padding: 0in 5.4pt;height: 19.55pt;vertical-align: top;">
                    <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;line-height:normal;'><span style="font-size:16px;color:#16191F;background:white;">10.0.248.0/21</span></p>
                </td>
            </tr>
        </tbody>
    </table>
</div>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:16px;">Deployment Steps:</span></strong></p>
<p><strong><span style='font-family:"Times New Roman";font-size:12.0pt;line-height:107%;'>1. Create VPC</span></strong><br><br><span style='font-family:"Times New Roman";font-size:16px;line-height:107%;'>1.1)&nbsp;</span><span style='font-family:"Times New Roman";font-size:16px;line-height:107%;'>I have followed the steps given in&nbsp;</span><a href="https://docs.aws.amazon.com/quickstart/latest/vpc/architecture.html"><span style='font-family:"Times New Roman";font-size:12.0pt;line-height:107%;'>https://docs.aws.amazon.com/quickstart/latest/vpc/architecture.html</span></a><span style='font-family:"Times New Roman";font-size:12.0pt;line-height:107%;'>&nbsp;to deploy this VPC of 10.0.0.0/16 CIDR block.</span><br><br><span style="font-size:16px;">The CloudFormation template was used to create a stack of resources. These resources are needed to be deployed for this architecture.<br> Stack name = <strong>&ldquo;OveshProject1&rdquo;</strong></span><br><br><span style="font-size:16px;">Stack ID =&nbsp;</span><a href="https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/stackinfo?stackId=arn%3Aaws%3Acloudformation%3Aus-east-1%3A672277104205%3Astack%2FOveshProject1%2F712677f0-49b8-11ed-a817-0a533431ff97"><span style="font-size:16px;">https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/stackinfo?stackId=arn%3Aaws%3Acloudformation%3Aus-east-1%3A672277104205%3Astack%2FOveshProject1%2F712677f0-49b8-11ed-a817-0a533431ff97</span></a></p>

<img src="/Images/Picture2.png" alt="Description of the image" width="1000">    

<div style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>
<p style="text-align: center;"><span style='font-family:"Times New Roman";font-size:16px;line-height:107%;'>1.2) This stack created 72 resources to deploy this architecture</span></p>
</div>
</p>
<center><img src="/Images/Picture3.jpeg" alt="Stack Creation Complete" width="713" ></center>

</body>
</html>
