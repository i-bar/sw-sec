## Main

[Troy Hunt's](https://www.troyhunt.com/owasp-top-10-for-net-developers-part-1/)

[Cool prez](https://www.catallaxyservices.com/media/OWASP-Top10-2017/#/)

## Adjacent

### SQLi
* [Hall of shame](https://codecurmudgeon.com/wp/sql-injection-hall-of-shame/)
* [Much cool info](https://www.catallaxyservices.com/presentations/sql-injection/)
* [Code snippets - bobby tables](http://bobby-tables.com/adodotnet_ef)

### Broken Auth
* [.NET Membership](https://docs.microsoft.com/en-us/dotnet/api/system.web.security.membership.enablepasswordreset?redirectedfrom=MSDN&view=netframework-4.7.2#System_Web_Security_Membership_EnablePasswordReset)
* [.NET Login](https://docs.microsoft.com/en-us/dotnet/api/system.web.ui.webcontrols.login.remembermeset?redirectedfrom=MSDN&view=netframework-4.7.2#System_Web_UI_WebControls_Login_RememberMeSet)

### Sensitive Data Exposure
* [Cisco Next Generation Cryptography](https://www.cisco.com/c/en/us/about/security-center/next-generation-cryptography.html)
* [Cryptographic Storage Cheat Sheet - OWASP](https://www.owasp.org/index.php/Cryptographic_Storage_Cheat_Sheet)
* [Nice Password Hashing tutorial](https://www.codeproject.com/Articles/704865/Salted-Password-Hashing-Doing-it-Right)
* [.NET Core Identity](https://docs.microsoft.com/en-us/aspnet/core/security/data-protection/configuration/overview?view=aspnetcore-2.1&tabs=aspnetcore2x#changing-algorithms-with-usecryptographicalgorithms)
* .NET Framework:
  * [Hash with SHA 512](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.sha512cng?view=netframework-4.7.2)
  * [Compute and add salt](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.rngcryptoserviceprovider?redirectedfrom=MSDN&view=netframework-4.7.2)
  * [Security namespace](https://docs.microsoft.com/en-us/dotnet/api/system.security?view=netframework-4.7.2) for Authorisation
  * [Example](http://www.obviex.com/Samples/Hash.aspx)
  * [Another example](https://www.csharpstar.com/csharp-hash-data-using-salt/)  
* [.NET Core](https://docs.microsoft.com/en-us/aspnet/core/security/data-protection/configuration/overview?view=aspnetcore-2.1&tabs=aspnetcore2x#changing-algorithms-with-usecryptographicalgorithms)
* Treat pwds like underware TODO link
* Why not implement your own alg.:
  * [See first comment](https://stackoverflow.com/a/27484425/777833)
  * 
* Use [SecureString](https://docs.microsoft.com/en-us/dotnet/api/system.security.securestring?redirectedfrom=MSDN&view=netframework-4.7.2) type for passwords;
* [NIST Recommendation for Key Management](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57pt1r4.pdf)
* [Enforce usage of FIPS-certified algorithms](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.cryptoconfig.allowonlyfipsalgorithms?redirectedfrom=MSDN&view=netframework-4.7.2#System_Security_Cryptography_CryptoConfig_AllowOnlyFipsAlgorithms)
* [msdn contra FIPS NIST](https://blogs.technet.microsoft.com/secguide/2014/04/07/why-were-not-recommending-fips-mode-anymore/) & a good explanation of FIPS NIST stuff.
  United States Federal Information Processing Standard (FIPS)
  An implementation of an approved cryptographic algorithm is considered FIPS 140-compliant only if it has been submitted for and has passed National Institute of Standards and Technology (NIST) validation.
* [Which alg is FIPS-compliant](https://social.msdn.microsoft.com/Forums/vstudio/en-US/b1c59dcd-9a51-408d-bdaf-9a625c3cf503/what-are-all-the-encryption-algorithms-those-supported-by-fips-1402-standard-in-net-framework-40) - answer on msdn.
* [More on the FIPS 140 validation from MS](https://technet.microsoft.com/en-us/library/cc750357.aspx#_CNG_Validated_Cryptographic)

* Secure keys: [relevant-ish answer](https://stackoverflow.com/a/2037093/777833) to [AES question](https://stackoverflow.com/questions/2037021/aes-encryption-and-key-storage)
* [Encripting credit card numbers in the DB](https://web.archive.org/web/20121017062956/http://www.di-mgt.com.au/cryptoCreditcard.html)
* Use [ProtectedData](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.protecteddata?redirectedfrom=MSDN&view=netframework-4.7.2) to encode and decode keys.




