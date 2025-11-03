## Preparation

1. Ensure all projects are updated to the latest deployed version.
2. Test the platform on Kubernetes.
3. Prepare the production environment variables and deploy the secrets to Kubernetes.
4. Restart the services to apply the updated secrets inside the containers.

---

## Migration

5. Prepare and test the migration script. Take note of the Load Balancer’s IP address and verify the Ingress configuration in Kubernetes.
6. Migrate the database to **OTC**.
7. Update the DNS records for both the backend and frontend to point to the **OTC Load Balancer** IP address.

---

## Notes

- It might be better **not to migrate the ElevenLabs redirector**.
- Add a new DNS to the ElevenLabs redirector **before** starting the process.
