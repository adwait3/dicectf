![image](https://github.com/adwait3/dicectf/assets/148553626/d71337e7-a1b2-4c5e-8491-026e40049d4e)# ZSHFUCK
## challenge
**may your code be under par. execute the "getflag" binary somewhere in the filesystem to win

"nc mc.ax 31774"
attachments
https://static.dicega.ng/uploads/53c6360b9ea7e5dba86f1d8d600de61b8601c1897b651eb88920906ff738f651/jail.zsh

## solution
in this challenge we were given a zsh file, zsh is basically like bash and is a shell scripting language , this was the file.

![Screenshot_2024-02-12_11-21-59](https://github.com/adwait3/dicectf/assets/148553626/a9415bca-17cc-47a2-a17e-52dce9e2d9e0)

in this file we see that we can choose a characterset of 6 to run our commands using those 6 characters only and we have to read the file containing the flag , but the twist tis there are some characters which are forbidden "banned = ('*','?','`')"
now this is what i tried first
![Screenshot_2024-02-12_11-21-19](https://github.com/adwait3/dicectf/assets/148553626/d58087b3-94ef-4471-94e7-bdf1ec4a9421)
there was a executable ./run so i tried running it as well

![Screenshot_2024-02-12_11-22-41](https://github.com/adwait3/dicectf/assets/148553626/da2e3bdf-23fe-4ad5-8bd7-1fbdc748f93c)
this called the character choosing function again but still we coudlnt update the characters and were stuck with the characters we begun with.
this question definatley required some wildcard characters and after thorugh research i found '[--~]' is a wildcard to match all alphae=bets and numbers and can be used in this question and it indeed was the answer.
![Screenshot_2024-02-12_11-31-23](https://github.com/adwait3/dicectf/assets/148553626/e655fac6-3fdb-4d3d-ba4f-5d03df5abc9c)
## flag
dice{d0nt_u_jU5T_l00oo0ve_c0d3_g0lf?}
