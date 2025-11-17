## Preparation

- [ ] Change webhooks of old agents to a new one
- [x] Check all webhooks are pointing to https://platform.voico.ai and https://api.voico.ai
- [ ] Check SSL Certificate of DNS domains are setup for the redirection
- [ ] Ensure all projects are updated to the latest deployed version.
- [ ] Test the platform on Kubernetes.
- [ ] Prepare the production environment variables and deploy the secrets to Kubernetes.
- [ ] Restart the services to apply the updated secrets inside the containers.

---

## Migration

- [ ] Prepare and test the migration script. Take note of the Load Balancer’s IP address and verify the Ingress configuration in Kubernetes.
- [ ] Migrate the database to **OTC**.
- [ ] Update the DNS records for both the backend and frontend to point to the **OTC Load Balancer** IP address.

---

## Notes

- It might be better **not to migrate the ElevenLabs redirector**.
- Add a new DNS to the ElevenLabs redirector **before** starting the process.
