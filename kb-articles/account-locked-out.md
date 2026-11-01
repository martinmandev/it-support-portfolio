# Account locked out

**For:** Service desk · **Applies to:** Windows 10/11, domain PCs

## Symptoms
- The user sees *"The referenced account is currently locked out"*.
- They may still know their password.
- The account may lock again shortly after being unlocked.

## Cause
Too many wrong passwords, either typed by the user or sent by a device still using an old password.

## Steps
1. **Verify the caller** with a callback to the number on file.
2. Open **Active Directory Users and Computers** and find the user's account.
3. On the **Account** tab, tick **Unlock account** and click **OK**. Ask the user to sign in while you're still on the call.
4. **If the account locks again:** on the domain controller, open **Event Viewer → Security** and filter for Event ID `4740`. Note the **Caller Computer Name**.
5. **Fix the source** on that device. Common ones:
   - a phone's mail app
   - saved credentials in **Credential Manager**
   - a mapped drive
   - an old Remote Desktop session
6. **If the user has forgotten their password:** right-click the account → **Reset Password**, set a temporary one, and tick **User must change password at next logon**. Give the temporary password by phone or through their manager, never in the ticket or by email. Otherwise, don't reset.
7. Wait **10–15 minutes** and check for new 4740 events.
8. **Document the ticket:** how you verified the caller, the cause, and what you did.

## If that doesn't work
Escalate to second line, with:
- the 4740 event details
- the Caller Computer Name
- what you've tried

**Related:** [Tutorial: Password reset and account unlock in Active Directory](../tutorials/02-password-reset-and-unlock.md)
