## Receiving machine
`sudo netcat -l -p 7000 | pv | tar x`

## Sending machine
`sudo tar cf - * | pv | netcat w.x.y.z 7000`

get `w.x.y.z` by running `hostname -I` on the receiving machine

this will transfer everything in the current directory on the sending machine to the current directory on the receiving machine

