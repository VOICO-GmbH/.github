## Preparation

1. Check all webhooks are pointing to https://platform.voico.ai and https://api.voico.ai
2. Check SSL Certificate of DNS domains are setup for the redirection
3. Ensure all projects are updated to the latest deployed version.
4. Test the platform on Kubernetes.
5. Prepare the production environment variables and deploy the secrets to Kubernetes.
6. Restart the services to apply the updated secrets inside the containers.

---

## Migration

7. Prepare and test the migration script. Take note of the Load Balancer’s IP address and verify the Ingress configuration in Kubernetes.
8. Migrate the database to **OTC**.
9. Update the DNS records for both the backend and frontend to point to the **OTC Load Balancer** IP address.

---

## Notes

- It might be better **not to migrate the ElevenLabs redirector**.
- Add a new DNS to the ElevenLabs redirector **before** starting the process.
