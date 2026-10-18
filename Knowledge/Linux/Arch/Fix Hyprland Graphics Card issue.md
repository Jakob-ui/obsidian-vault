To show all the gpu cards **(Nvdia often ends with "01:00.0", iGPUs with "00:02.0")**: 
`ls -l /dev/dri/by-path/` 


Here the primary card has to be the nvdia one. For example, when nvida is card1 and intel would be card0:
`env = AQ_DRM_DEVICES,/dev/dri/card1:/dev/dri/card0`

After update build init frames:
`sudo mkinitcpio -P`