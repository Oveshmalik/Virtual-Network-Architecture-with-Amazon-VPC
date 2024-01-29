
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
    <img src="/Images/Picture1.png" width="1000">    
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

<img src="/Images/Picture2.png" width="1000">    

<p>1.2) This stack created 72 resources to deploy this architecture</p>
<img src="/Images/Picture3.png" width="75%" >
<img src="/Images/Picture4.png" width="100%" >
<p>1.3) VPC Instance OveshProject1 has been created with stack and can be found under Your VPCs tab</p>
<img src="/Images/Picture5.png" width="75%" >
<p>1.4)	All the corresponding subnets have been created as per the CIDR and IP addresses have been assigned in each subnet. The number of available IP addresses are matching with the VPC architecture requirements.</p>
<img src="/Images/Picture6.png" width="100%" >
<p>1.5)	The Route tables were created to route the traffic within the VPC. Private Subnets can access the Internet via a NAT Gateway using a route map.</p>
<img src="/Images/Picture7.png" width="100%" >
<p>1.6)	4 NAT Gateway were deployed here and placed in Public subnets in each availability zone</p>
<img src="/Images/Picture8.png" width="100%" >
<p>1.7)	Internet Gateway was created and attached to the VPC for Internet access</p>
<img src="/Images/Picture9.png" width="75%" >
<h4>Task 3) Secure the VPC with Network ACL & Security Group</h4>
<p><strong>3.1) Network ACLs</strong></p>
<p>To secure the VPC I have used the Network access control Lists(ACL) and security group to distinguish the access for each subnet in VPC. &nbsp;Lets begin with Network ACLs.</p>
<p>The goal of this architecture is security; Private Subnets should not accept any traffic from the outside world, however, they should be able to access the Internet and other subnets within this VPC</p>
<p>To do so, I have placed ACLs on all Private subnets in all availability zones where I have set the Inbound rule to deny all traffic from source 0.0.0.0/0 (Internet). Refer to the Inbound rules mentioned in Figure 14</p>
<p>Since private subnets are allowed to have Internet access I will put an outbound rule where I will allow the HTTP and HTTPS traffic destined to 0.0.0.0/0 (Internet). This should allow private subnet A in all availability zones to access the Internet. Refer to the Outbound rules mentioned in Figure 16</p>
<img src="/Images/Picture10.png" width="100%" >
<p><strong>3.2) Security Groups</strong></p>
<p>3.2.1) I have created this security group for Public subnet located in Availability Zone 2. Public subnets are supposed to be accessible from local VPC network and can be accessible from outside  Interenet using RDP secure connection. The Inbound rules set below(refer to figure 17) will satisfy the conditions.<br>
Public subnet should be able to access the Internet so in outbound rules I will set all traffic from all ports destined to 0.0.0.0/0</p>
<img src="/Images/Picture11.png" width="100%" >
<p>3.2.2) Another security group is created for Private subnet A located in Availability Zone 2. I have created an exception here where I will allow Public subnet 10.0.144.0/20  from availability zone 2 to access this private subnet using RDP connection in the Inbound rule. Private subnet will only reply to the RDP request which is defined in the outbound rule. (Refer to Figure 18)</p>
<img src="/Images/Picture12.png" width="100%" >
<p>This will be demonstrated with EC2 Instance in further steps under <strong>Deployment of EC2</strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:19px;">Task 4: Deploy the follwing Services :</span></strong><strong><span style="font-size:16px;"><br>&nbsp;EC2 &nbsp; &nbsp; &nbsp;S3&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;CloudWatch&nbsp; &nbsp;CloudTrail&nbsp; &nbsp; &nbsp; &nbsp;TrustedAdvisor</span></strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><u><span style="font-size:16px;">4.1) Deployment of &nbsp;EC2</span></u></strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">4.1.1) I created a key pair to access my EC2 Instance using the RDP secure connectio. RSA as the encryption type and the format of the key was .pem. &nbsp;</span></p>
<img src="/Images/Picture13.png" width="65%" >
<img src="/Images/Picture14.png" width="60%" >
<p>4.1.2) To demonstrate the VPC architecture and its functionality I have deployed 4 EC2 Instances in total. Where 2 Instances are located in Availability Zone 1, and the other 2 are located in Availability Zone 2. Both Availability zones have Windows Server 2022 Base instance for 1 public Subnet and 1 Private Subnet.<br> 
I am configuring an Instance for Public Subnet 10.0.144.0/20 in Availability Zone 2. I used a free tier-eligible OS image  for the Instance type.</p>
<img src="/Images/Picture15.png" width="65%" >
<p>4.1.3) I mentioned the Key Pair I created earlier with the name Ovesh_PRJ1. It will be used for login purposes.
In Network settings under VPC selection, I selected VPC name OveshProject1 which I created using the CloudFormation template earlier in Task 1. In subnet selection, I selected Public Subnet 2 with the CIDR 10.0.144.0/20 as we are deploying a server for this CIDR block.</p>
<img src="/Images/Picture16.png" width="65%" >
<p>4.1.4) For the Firewall I selected the security group Public Server SG that I mentioned earlier in Task 1 under the title security group. Lastly, I attached a free tier storage to my server instance and clicked on Launch instance to deploy it. These steps were repeated to create other 3 Instances with their respective availability zones and Private/Public subnet CIDR. </p>
<img src="/Images/Picture17.png" width="65%" >
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:16px;">Availability Zone 1:<br>&nbsp;</span></strong><u><span style="font-size:16px;">Instance Name:</span></u><span style="font-size:16px;">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<u>CIDR</u><strong><br>&nbsp;</strong>project1-private-ovesh&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;10.0.0.0/19<br>&nbsp;project1-public-ovesh&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;10.0.128.0/20<br>&nbsp;</span></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:16px;">Availability Zone 2:<br>&nbsp;</span></strong><u><span style="font-size:16px;">Instance Name:</span></u><span style="font-size:16px;">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<u>CIDR</u><strong><br>&nbsp;</strong>Ovesh_PrivateSN_AZ2&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;10.0.32.0/19<br>&nbsp;Ovesh_PublicSN_AZ2 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;10.0.144.0/20</span></p>
<p>4.1.5) Our EC2 Instances for above subnets have been created.</p>
<img src="/Images/Picture18.png" width="100%" >
<p>4.1.6) I have downloaded the RDP client(Refer to Figure 22) for all 4 Instances and I will be using the same key pair <strong>Ovesh_PRJ1.pem</strong> to decrypt the password for all instances
I decrypted my RSA key <strong>Ovesh_PRJ1.pem</strong> and copied the password to use for authentication. </p>
<img src="/Images/Picture19.png" width="55%" >
<p>4.1.7) I will connect to Public subnet 10.0.144.0/20 located in Availability Zone 2 using Remote Desktop file Ovesh_Public_AZ2.</p>
<img src="/Images/Picture20.png" width="60%" >
<p>4.1.8) The security group policies will allow authorized users with the valid key pair to access the Instance using RDP from anywhere.</p>
<img src="/Images/Picture21.png" width="100%" >
<p>4.1.9) As we can see below the connection has been established and I can access the Public Subnet 10.0.144.0/20. My private IP address is 10.0.153.23 which is within CIDR /20 range,  where the first IP address is 10.0.144.0 and the last IP address will be 10.0.159.255. NAT gateway assigns a public IP address 174.129.66.97 to communicate to the outside Internet.</p>
<img src="/Images/Picture22.png" width="100%" >
<p>I will now connect to Private subnet Instance <strong>Ovesh_PrivateSN_AZ2, 10.0.32.0/19 </strong> from my local machine.</p>
<img src="/Images/Picture23.png" width="80%" >
<p>4.1.10) It won’t connect for one of the reasons that is mentioned in the error message. The reason is that the security group assigned to this subnet restricts all traffic and only allows an RDP request from the Public Subnet 10.0.144.0/20. This subnet will only reply to that RDP request as mentioned in the outbound rule.</p>
<img src="/Images/Picture24.png" width="60%" >
<p>4.1.11) Now let's connect this from Public Subnet 10.0.144.0/20. It worked because it matches the security group policies mentioned above in the figure .</p>
<img src="/Images/Picture25.png" width="100%" >
<p>4.1.12) To demonstrate further, I have enabled Internet access on both, Public and Private Subnets. As per the architecture requirements, the private subnet can ping the public subnet but the Public subnet is not allowed to access the private subnet. This was achieved by setting the group policies on EC2 Instances </p>
<img src="/Images/Picture26.png" width="100%" >
<p>This shows that our VPC architecture has been created and it is secured by applying the  Network ACLs and Security Group at subnet level and instance level.</p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:16px;">4.2) <u>Deployment of CloudWatch</u></span></strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">4.2.1) Cloudwatch allows you to monitor the activities of your resources in AWS by the implementation of Alarms on your resources. It notifies the user using an SNS notification when certain conditions are matched on set alarms. I will demonstrate the cloudwatch by setting 2 alarms on the EC2 instance that I have created Availability Zone 2.</span></p>
<p><span style='font-size:16px;font-family:"Calibri",sans-serif;'>I navigated to <strong>CloudWatch</strong> from <strong>Services</strong> section in AWS console. I clicked on &nbsp;&ldquo;<strong>Create Alarm</strong>&rdquo; option in Cloudwatch and then click on select metric.&nbsp;</span></p>
<img src="/Images/Picture27.png" width="65%" >
<p>4.2.2) I wanted to create the alarms on my EC2 Instances so I selected <strong>EC2</strong> under Metrics tab.</p>
<img src="/Images/Picture28.png" width="80%" >
<p>4.2.3) I will create an alarm that will notify me the CPU usage of my Public server running in the Public Subnet of Availability Zone 2. For this alarm, I have searched the term CPU utilization in the search bar and selected my Public server Ovesh_PublicSN_AZ2. </p>
<img src="/Images/Picture29.png" width="100%" >
<p>4.2.4) I want an alarm to be triggered every 1 minute when CPU Utilization exceeds 35%. To do so, Under the Metric tab, I have selected Sum as my calculation method in the statistics option and 1 minute for time in the Period option. Under Conditions, I have selected the alarm condition as Greater/Equal to 35 threshold value. </p>
<img src="/Images/Picture30.png" width="65%" >
<p>4.2.5) I want to receive emails about my CPU Utilization alarms. In this step, I have created an SNS topic under the <strong>Notification</strong> tab. I have given the topic name Ovesh_Project1_Public_CPU_Utilization(this will be the subject of the email) and mentioned my Seneca email address where I want the emails to be received.</p>
<img src="/Images/Picture31.png" width="65%" >
<p>4.2.6) I repeated the steps mentioned above to create one more Alarm on my Private server running in the Private Subnet of Availability Zone 2. This Alarm (Ovesh_Project1_Private_Networkpackets) will send me an email when 512 bytes of data are sent out by the Server. So, I have successfully created the Alarms on my Ec2 instances and Alarms are sending out the SNS notification to my email address. </p>
<img src="/Images/Picture32.png" width="100%" >
<p>4.2.7) Dashboard in Cloudwatch provides an overview of your resources in different representational formats. I have created a Dashboard for both of my Instances and I am using the graph to visualize the utilization of both Instances.</p>
<img src="/Images/Picture33.png" width="100%" >
<p>4.2.8) <strong>Alarm1</strong> is set on <strong>Project1-public-ovesh EC2 Instance.</strong> I am also able to see the detailed overview of my CPU utilization by navigating to <strong>Alarms</strong> section.</p>
<img src="/Images/Picture34.png" width="100%" >
<p>4.2.9) When CPU Utilization exceeds 35 % alarm will go off and it will send an SNS notification to my email address</p>
<img src="/Images/Picture35.png" width="65%" >
<p>4.2.10) Alarm 2 is set for <strong>Project1-private-ovesh EC2</strong> Instance. Figure 42 provides a graphical overview  of packets leaving the network over time.</p>
<img src="/Images/Picture36.png" width="100%" >
<p>4.2.11) The Alarm is set for outgoing network packets. When network packets of more than 512 bytes leave the network this alarm will trigger an SNS notification to my Email address</p>
<img src="/Images/Picture37.png" width="65%" >
<p></p><strong>4.3) <u>Deployment of CloudTrail</u></strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">4.3.1) Cloudtrail lets you log the management activities performed on AWS resources for review and audit purposes. I have created a trail by accessing <strong>CloudTrail</strong> feature located in Services tab. I named my trail as &ldquo;<strong>EC2-Public&rdquo;</strong> and I selected to log these files in an existing<strong>&nbsp;S3 bucket</strong> named <strong>ovesh-project1</strong>. I will add a folder <strong>EC2-CPU-Utilization-Log</strong> under which all these logs will be saved.</span></p>
<img src="/Images/Picture38.png" width="60%" >
<p>4.3.2) Once the Trail has been created, I can make changes needed later by simply clicking the Trail name in the Dashboard. I can stop the logging of events by clicking on the Stop Logging option. And when I no longer require logging the events, I can simply delete this trail as well.</p>
<img src="/Images/Picture39.png" width="100%" >
<p>4.3.3) Dashboard allows me to check the status of all my Trails and provides even history.</p>
<img src="/Images/Picture40.png" width="100%" >
<p>4.3.4) Log files generated through Cloudtrail are available in Event History, brief details regarding the Instances are provided here. </p>
<img src="/Images/Picture41.png" width="100%" >
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong><span style="font-size:16px;">4.4) <u>Deployment of S3</u></span></strong></p>
<p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">4.4.1) I deployed an S3 Bucket name <strong>ovesh-project1&nbsp;</strong>to store the Log files generated from the Cloudtrail events.</span></p>
<img src="/Images/Picture42.png" width="100%" >
<p>4.4.2) After the bucket is created we can verify it on the S3 dashboard. All buckets created will be shown here.</p>
<img src="/Images/Picture43.png" width="100%" >
<p>4.4.3) ovesh-project1 bucket that we created has 2 folders in it name <strong>EC2-CPU-Utilization-Log/</strong> and <strong>Public/</strong>. These 2 folders were created during the creation of CloudTrail to log the events of my deployed instances </p>
<img src="/Images/Picture44.png" width="100%" >
<p>4.4.4) The logged events from CloudTrail are being stored in <strong>ovesh-project1</strong> S3 bucket under the <strong>Public</strong> folder and it creates the subdirectories for each day and store the logs in it. </p>
<img src="/Images/Picture45.png" width="100%" >

</body>
</html>
