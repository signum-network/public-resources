# Signum Public Resources

This is a auditable and transparent web application that allows developers to seamlessly fetch a list of Public Signum resources like for example Nodes, Mining Pools or third-party apps powered By Signum into their applications. The primary objective is to enhance the overall developer experience.

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

### Third Party Apps
```bash
curl -X GET "https://signum-network.github.io/public-resources/third-party-apps.json" \
 -H "Accept: application/json" 
```

# Developer Section

## Public Nodes
We only show the featured nodes stated by the [Signum Explorer Nodes List](https://explorer.signum.network/peers/) and [Signum Explorer Testnet Nodes List](https://testnet.explorer.signum.network/peers/)


## Mining Pools
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

## Third-party Apps

If you want to add a `App` which uses heavily the Signum Blockchain, you have the posibility to show it off to the community by listing it on third party apps list. `(on the next section you will learn how to do it)`.

### Important Tips

- Centralized Exchanges are not allowed, they are listed on another signum documentation site.

```
You must request listing by creating a pull request on this repository
```

### Adding a third-party app

You will need to create a PR in order to add the third party app. 

- Go to `third-party-apps.json` file
- Copy the following template and change it according to your website data


**Template**
```json
    {
      "title": "Signum DApp",
      "description": "This is a DApp powered by the Signum blockchain",
      "img": "Absolute URL of an image logo",
      "url": "https://app-website.com/"
    },
```
**Recommendations:**
- You must keep the `title` and `description` short 
- `URL` must be the link of the website
- We recommend the following for the image `(img)`
  - Logo
  - Size: `75x75`
  - File type: `.jpg` `.png` `.webp`


**Example**
```json
    {
      "title": "SignumArt",
      "description": "A NFT portal on the Signum blockchain",
      "img": "https://signumart.io/assets/img/seo.jpg",
      "url": "https://signumart.io/"
    }
```

- If the app is on the `Mainnet`, insert the object into the `Mainnet Array`; however, if the app is on the `Testnet`, insert the object into the `Testnet Array`
- Once you add the app to the list, then you can create your PR


# Disclaimer

*Kindly be aware that all the links provided in this website are solely for your convenience and informational purposes. Their inclusion here does not imply any endorsement by the Signum community of the products, services, or opinions presented by the mentioned corporations, organizations, or individuals. The Signum community assumes no liability for the accuracy, legality, or content of these external websites. If you have any questions about the content on those sites, please reach out to the respective site's administrators. Remember to exercise caution and perform your own research before making any online purchases; "buyer beware" always applies. Always use your best judgment when navigating the digital landscape.*