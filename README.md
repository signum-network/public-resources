# Signum Public Resources

This is a auditable and transparent web application that allows developers to seamlessly fetch a list of Public Signum Nodes or Mining Pools into their applications, with the purpose of improving the overall developer experience.

# Fetching Resources

### Public Nodes
```bash
curl -X GET "https://signum-network.github.io/public-resources/nodes.json" \
 -H "Accept: application/json" 
```

### Public Mining Pools
```bash
curl -X GET "https://signum-network.github.io/public-resources/pools.json" \
 -H "Accept: application/json" 
```

# Developer Section

### For those who want to add a pool

If you want to add your a Mining Pool to the list of pools, you just need to make sure that is compatible with [`Signum-pool`](https://github.com/signum-network/signum-pool) mining protocol

#### Once you comply with the requirements.
You will need to create a PR in order to add your pool. 

- Go to `pools.json` file
- Copy the following template and change it according to your pool data


**Template**
```json
    {
      "id": "your-pool-unique-name",
      "name": "Your Pool Unique Name",
      "url": "https://your-pool-unique-url.com"
    }
```
> URL must be the mining URL which miners will send "deadlines"

**Example**
```json
    {
      "id": "my-signum-pool",
      "name": "My Signum Pool",
      "url": "https://my-signum-pool.com"
    }
```

- If your pool is mining on the `Mainnet`, insert the object into the `Mainnet Array`; however, if your pool is mining on the `Testnet`, insert the object into the `Testnet Array`
- Once you add your pool to the list, then you can create your PR

### Public Nodes
We only show the featured nodes stated by the [Signum Explorer Nodes List](https://explorer.signum.network/peers/) and [Signum Explorer Testnet Nodes List](https://testnet.explorer.signum.network/peers/)

# Disclaimer

*Kindly be aware that all the links provided in this website are solely for your convenience and informational purposes. Their inclusion here does not imply any endorsement by the Signum community of the products, services, or opinions presented by the mentioned corporations, organizations, or individuals. The Signum community assumes no liability for the accuracy, legality, or content of these external websites. If you have any questions about the content on those sites, please reach out to the respective site's administrators. Remember to exercise caution and perform your own research before making any online purchases; "buyer beware" always applies. Always use your best judgment when navigating the digital landscape.*