## Preparation

1. Check all webhooks are pointing to https://platform.voico.ai and https://api.voico.ai
2. Ensure all projects are updated to the latest deployed version.
3. Test the platform on Kubernetes.
4. Prepare the production environment variables and deploy the secrets to Kubernetes.
5. Restart the services to apply the updated secrets inside the containers.

---

## Migration

6. Prepare and test the migration script. Take note of the Load Balancer’s IP address and verify the Ingress configuration in Kubernetes.
7. Migrate the database to **OTC**.
8. Update the DNS records for both the backend and frontend to point to the **OTC Load Balancer** IP address.

---

## Notes

- It might be better **not to migrate the ElevenLabs redirector**.
- Add a new DNS to the ElevenLabs redirector **before** starting the process.
