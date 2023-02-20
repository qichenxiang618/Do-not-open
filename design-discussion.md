## Section 1 - Individual Designs

Design 1

![Alt Text](https://lh3.googleusercontent.com/5K_L14jds8ZVghEovfBlD8hp6OeiHSFWhkaMVjmjA-F169RrO2rHibzEQFi1p_LsGp3qEQUyvats5UO25QBpV0ny-xtZFKaZsQL7Q3akSqCgnjNlYl-jpVYi7_eY0K_RefCYzkmP_zd28EEth9LmC1OsL6samkPFnqv_mYADxUxaYff6dDcHhCAPorraHDMT5D5cu-966QaO0P1LPqeDXKB-r5RnqCHolJjiMxmDJMKtxK6m4g55-lyWbwmakLE9_XS6JLs-J0C2P-ZMe759-MLU3C-SyDifVx9twrwu4pE1tGd0AI910dpLwb8OBXneGyzzaInKFxlbTiRlCEnc7SXBBM0a6RjpgITL2A-8km2w2S3X5RkFYvC4q6R_dd-Gmb2ACLLAwVARiXGvf89K2maeFz_rTneYjjeAqWDaR-XC7cEeiaeliXSH-puPukeXuFxU5rt-SnEnJC4GIKQI-6tCfdPobLmzP1ol5l-xkBlUG-IO-xMOcP6gRmon8jfRhKIdC1gIK2xzVKXUrdJ4FbLATQcUwWKuWdM2By8cldplpj9qDRomGPwVG4f8Po7JQzd6pBfvpnJ9i8UE_617wBBC_I15rhLdsxplKrQnfzJVqil_4n6zODSgVhKQ69uRRuoS9eshTcDgyd9kY29f2dypbRWSuHaC8sYBLgV1bF_365jfALgW0zzbAoHl2jiNEyWrWzuw_s0j0RLEUI24TnxkJPILTUcP6jXoQniAsE27aoXEsugbQjpxZZ6lkkQR1-2cnaH-josPbZA2Le-J1FzTp03D9_kGPi1rOpTFMZU5kB0Jpt3xi87ZwehOWht400gbcjzxv8vLSnCE9gmZf57Yd33SZ1mDp0zDwfXFYompH9qrsWYZj_AlMpYDTasGC4SxzusNuLRHM3VMRz8zZKYu6Kx_BiKVooH4QQVm5p0RKR5eXUg17FojXPWR8JbdVcpLFHx95bXeZEeoJMG-If6QIDUqZmpYD6vSOXSHGbCzvMBgNF9D=w1131-h520-s-no?authuser=1)

Pros:
- This design has 2 child classes: CurrentJob and JobOffer which is advantageous because CurrentJob will be editable whereas a JobOffer object will not be

Cons:
- MainActivity class should have an attribute to store an array of JobOffer objects, and an attribute to store a CurrentJob object
- Weight attributes should have default values
- Company class was originally designed to avoid duplicate information and save space, but since the dataset is small, it is not necessary and should be combined to the Job class
- Some methods should have parameters types


Design 2

![Alt Text](https://lh3.googleusercontent.com/tbc0PeXsHnHtGFyeiuTCvHECLnSMUhmrSjjDOjo_G2Kw4W-c5xRZhkXqjTkUpYFE4HMmvyr-dX5D6K99aOerLr8j1FwP15GOug09N8u6pDRtRyUTcr2GfMtLYg_X8STqVWqsVhg21B-wgS9gIjDS3LyzASmLxQP7j1y-s39pNIHktgqumqex3lOzRYDfexCxc9kvN0IYXHu-WB8SQV_PIdLR-I2YZlCJRwRwAGabvFJijwAoIXroD70zaxUaHW5mB_1HsmBXOsGIwhS0l1A9lWdCa_N2sXFxHQgP9c68hTyDFjwTReSEVnFsJi26Q88JRRKFF4-MOkm4S4HBl3YHoUV9slsyho41Wnmfktef2fGSfMcrHt8N98ScFBEsd9cT9iG0GRKEr1QMw4kQkApvET40OZzKeLMusiy-1waPmjyH0mNbZFHRS2yhuMPpCwtvFXOw8d6HEZ7VGi8LnI5lTynpO3FtQTSsU16xFN0RMjF3ZlSovXUdXZUILw9o-3vecj7cbc3vm-Ja0pLC2JTygHZ4MfacJCHILUOkblWQj9IXZo4DlPLUPhZb5VnKYZ8lzQaL7PJH7rgzkvWv8RvxqLWDLLDONr6fHgRcWv5eN_2h0em9MfeuNRD9vuiCxc4Q-3CrGdRjNZDlCIuYbg8M0ScEMdMP9eaVW8nSeQtx0uCChEyWGfWd79ffV7Aiiwo95GOcv8W79DdRw_Iytpio4Xi1tap3JihahCwFs_8uNmzmFJAsRhlDVeeW-b0j71DFqu6ATqD4ae7WiTcjjwq-y8lTkigqm274348gU16THu4SVKFnzErPao7-rfv6SvWppTBOD3ImsWHDmjwfxaxBAnh7bnLJZ2XlgjYP6oNg9EBK1M9wS2fePs3qWsjMhGwYO1BdaPOG6j4I6h57tqjxZPb_k2Lqlpjuo7mz_JYGqJ9RppZuGpuqNQHYwwiF2FsFw1eOzHsvf_G9fnZfmd5-C7g6hKyaD_376jMeAO2Ou9rpIL72mmwY=w531-h634-s-no?authuser=1)

Pros:
- This design has 2 important utility classes: Money and Location
- The JobOffers.score attribute is correctly labeled with ‘/’ indicating it is a derived attribute

Cons
- Class names should be in singular form. ‘JobOffers’ should be called ‘JobOffer’
- The current job should be represented as a subclass not just as an attribute since it has some of its own functionality


Design 3

![Alt Text](https://lh3.googleusercontent.com/8GrjwdwErvdp3fj6EG516EagNqZXacBrX5E0az_ypa34gvHhHwL8KE6z_JkOYAc_FDY4nHNr6CNCwgpjpzP_rhMf1zG3xXi9TLf0epLTHphKEAPKPMqKj7L98RmFLObG8cVbp6K_E1wUXkR7fu9kx1TcTp5fdq5yL_OUwtMuLzLt78N4VaC7gr2lTPlbAJ_hcOgeG8eTzOiLNKt2Zd_GKgayMeKMHU1AXmomrB2jpS5IzSXuL24rc5DnHyFk_9lN6hqk5No2d1s8CSNs1Fx7PnW3Vp58iwGP-MjQO4JK8bP2yjFxBIl4THlsgj6uSf1sQCVolr2Mw4jROu7TC8v9srtzJ_Ze3Ec--A749rBGN2tqhGzOpzMDYZrW1ux-T32u-o-DOFP8nyszlheHymL8DV2sLLSaEaZUk-QMgBwHhFf4xHXif0BNnYrcKwcgS3TYZ-VmOA3Lzuk4a__yOhwhNv2qy3n-pBkQy-xTlxA-spWoWOjSSXjtF5Bf0Ls4CE0BemgpfdzPhW6Vsqat_OW9XS_lDciFhr8F0XBpRNEjAIKTp_jJzpc_MdT6rFAqT1PEhIeM2DhG11OjvkkFR_kamqSM1kKoz0e8SxEbUb-ru2mbfrXvnzqTygIpSDZTPsYspdPv3-59_3S6AeUCQTG8sCICbV9K351B78poxNhM-ywQPnedEBu5moLlJTyNRdtSRIJrR4M_qiKI5bLRB4kIX7Epp6HK0HQvQdnLdjd8zi3Eb_7rLkC2yMVDm7nrM9NS94wQ-6tRVTqbhinfMOTORlMiCCeAIvZXCG9joINssgAip8Y7PianQZrKix2Rg0GV1aUxO4mLzZ6g9yFzFRXtaCKa4H4VhxFoguSQvz__fe-1AGrv7aG91eh715GjlyUn-IGq8ajBIyPWblUQj3p6Zar3kfPqJToZd2EJbKOCfR5dnP4YlcCZ156RY6e6ykFcv87-Rv-X-omw7oolWxvQVKKBR_uuPOrjkRSXVv84gGnDxQM7toFy=w1079-h451-s-no?authuser=1)

Pros:
- This design has method parameters, including parameter names and data types
- This design has default values for those 5 weight attributes

Cons:
- The User class should be called MainMenu or MainActivity class, as there is only 1 user
- Weight attributes should be in the MainMenu/MainActivity class
- The Offer class is not needed


Design 4

![Alt Text](https://lh3.googleusercontent.com/LSjk22W2nVp1BI8V3BFeROX1XM_7LWjiUgxw2d0kr3Mtujr4s7A8vmkOXvZFEV9C7RsRSjapo_IEZErfUl0I_uUP6bqvRY26AjxLMIloiZAFIax0VL56sR7IWXAWrGvq7cKr-u4lp8o6U_tKoz3AYDyDPrEC2BO7X-gp6cVS3MJOokCrsdEV6F509BCCx5K72qBcKaSCfs5LrL-SzCNY1KLxWepx3rJRrELj_0bO7AATJVfrRUgSoCUOidP9q5JrQEBwuTpvVvi6b0ak5NTgTlXCICEnZ6uNLDPx0dHlXuPpNQnSEWJzIhKY9NW-MSqIM19dHb7S-HrnV5THo4z1FwkPpovYC0eLHWFHgsAbP5i-U1-CU_ViHpqLCAYTZdw-c5T-8O8YCRSghkRP7vDcObeEDzO79sPccLvaeNipdLgPUx0BOlaTMNAHb1aXhyywfPV8IbA0O-LsvH9bEX0mmCj4MpwXG9f6kasClFm9Fz_JNUnQeiGMgXH3sTVJ5p7ZwJa_xiXANKPNHY-qbKQa6tHvcIlLCwUz616awSDA8MJvlx3G4uREyQlphuNiI86qHBNqFsvltPAtN8WQ_jK7mlwpIwlwN13Y4wxB0eMNA0BecrXpTRXF3m9LuQw7uXlgOjcGi117iv_Q9MogfLK3rxlwlHKr1TpWiBqE78X-nZTgOijY-zzxdLOBhe77epp_Yodb-gZJkofMIK3hLrtEoX0ZRsBUk-Bk1_DexXWeWLB96uJl-rJAialCZkDkAJcUIO-DWpn9NG_FY7WYRmvaQfMAy7wMSsm6cW5B_yrfCgEfP_zDLcvTzlEzKRs3_B7ZtzYWQ7AU8isiurU_D9gy1P90ZgDsEQkp8NiI0nYUaukHd8e-VFvv3FReU7QuCv6JB7d3-RDMEiKbgOwLznsJdnI0f-a3vgU4uBMWmaBj04qIAGW7gG61j0Iin43jWQp6P0t7fScPnkAz_h1sDN-rhGccgFHLNw0a1hPyt4UdPve_ipKyQ0av=w994-h904-s-no?authuser=1)


Pros:
- Attribute data types are correctly defined and labeled

Cons:
- JobComparison class and ComparisonSettings class are not needed, their attributes and methods should be in the MainMenu class
- Should have a super class Job that contains all the shared attributes of JobOffer class and CurrentJobDetails class, instead of having the same set of attributes in 2 classes
- Although not used in the P3L2 demo, it would be better to include cardinality and visibility symbols
- Some methods such as cancel() will be implemented on GUI, therefore are not needed in UML
- Class names should be singular


## Section 2: Team Design

Main commonalities
- Share a form of a MainMenu class which functions as the entry point of the app and contains most of the important user-specific attributes and methods.
- Share a form of a Job class which contains job specific attributes and is inherited by CurrentJob and JobOffer classes
- Store jobs in the form of an array or list in the MainMenu class
- To implement encapsulation, class attributes are set to private and methods are set to public, so that other classes can only access methods not attributes of other classes.
- Both team design and individual designs have visibility symbols, cardinality symbols, default attribute values and method parameters.

Main differences
- Some designs have separate jobOffer comparison classes whereas as some designs make the comparison feature a function of the Main class
- The team design has 2 child classes CurrentJob and JobOffer under the superclass Job, whereas most of the individual designs have only a single Job class. 



## Section 3: Summary

(Summarizes the lessons learned in the process of discussing the designs, in terms of design, team work, and any other aspect that the team members consider relevant.)

Lessons Learned
- Helpful to cross reference designs to verify every requirement is properly accounted for.
- Working with people with different perspectives and expertise can ensure that the diagram accurately capture the requirements
- Examining the designs of others can assist in identifying the areas of knowledge that we may be lacking.
- A requirement can often be fulfilled by multiple feasible approaches, each of which has its own advantages and disadvantages.

