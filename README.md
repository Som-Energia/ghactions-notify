# ghactions-notify

Github action to notify SomEnergia team on failing ci.

This action centralizes notification logic to have
a single point of modification, just in case
we want to change the way we get modification
in all the repositories.

Add this step on your workflow job:

```yaml
      - name: Notify
        uses: Som-Energia/ghactions-notify@main
        if: always()
        with:
          webhook: ${{ secrets.WEBHOOK_ALERTES_WEBAPPS }}
```




