<p align="center">
  <img src="https://github.com/esrayildiizz/Example/assets/106755194/e0197438-b265-449a-a90b-cf4f526a0e01" alt="PAYGATE Image"/>
</p>

<p align="center">
<strong>PAYGATE</strong>
</p>

<p align="center">
PayGate ile tüm online ödemelerinizi tek merkezden yönetin 
</p>
<p align="center">
katma değerli servislerimiz ile ödeme giderlerinizi azaltın, cironuzu artırın ve işletmenizi büyütün.
</p>

## PAYGATE
[![Paygate Dotnet CI](https://img.shields.io/badge/Paygate%20Dotnet%20CI-passing-brightgreen)]()
[![nuget](https://img.shields.io/badge/nuget-v1.0.61-blue)]()


## Gereksinimler
- .NET Standart 2.0
- .NET Core 8 (Tests ve Web projeleri için)

## Kurulum
`Install-Package  ...... `



## Kullanım
PayGate API'sine erişmek için öncelikle API kimlik bilgilerini (örneğin bir API anahtarı ve gizli anahtar) edinmeniz gerekir. 

API kimlik bilgilerinizi aldıktan sonra, PayGate kimlik bilgilerinizle bir örnek oluşturarak PayGate'i kullanmaya başlayabilirsiniz.

## Örnekler

### Kredi Kartı Ödeme Kullanım Örneği

```ruby
payment = PaymentService.new
request = CreatePaymentInput.new(
  amount: BigDecimal('100.0'),
  paid_amount: BigDecimal('100.0'),
  wallet_amount: BigDecimal('0.0'),
  installment: 1,
  conversation_id: "456d1297-908e-4bd6-a13b-4be31a6e47d5",
  currency: Currency::TRY,
  payment_group: PaymentGroup::LISTING_OR_SUBSCRIPTION,
  card: CardDto.new(
    card_holder_name: "Haluk Demir",
    card_number: "5258640000000001",
    expire_year: "2044",
    expire_month: "07",
    cvc: "000"
  )
)
response = payment.create_payment_async(request)
assert_not_nil response
```


### Katkılar
For all contributions to this client please see the contribution guide here.

## Lisans

*MIT*
