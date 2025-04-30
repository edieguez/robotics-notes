# CloudWatch alarms

Can be used to trigger a notification or an action if a certain condition is met. This is using metrics to monitor the health of your resources and applications. **Composite alarms can be created by combining multiple alarms**.

Alarm states are

1. `OK`
2. `ALARM`
3. `INSUFFICIENT_DATA`

Other services can react to alarms, like

- **Auto Scaling**: to scale in or out
- **EC2**: to stop, terminate, or recover an instance
- **SNS**: to send a notification
- **EC2 Actions**: to reboot or stop an instance
- **CloudWatch Events**: to trigger a Lambda function
- **CloudWatch Logs**: to log an event
- **CloudWatch Alarms**: to change the state of another alarm
