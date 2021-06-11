---
title: Работа с цифровыми подписями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- цифровые подписи [infopath 2007], InfoPath 2007, цифровые подписи
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Объектная модель Microsoft. Office. Пространство имен InfoPath предоставляет функции для программной работы с цифровыми подписями.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425577"
---
# <a name="work-with-digital-signatures"></a>Работа с цифровыми подписями

Объектная модель [Microsoft.Office. Пространство имен InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет функции для программной работы с цифровыми подписями. 
  
## <a name="digital-signature-features"></a>Функции цифровых подписей

Предоставляемые в InfoPath функции цифровых подписей позволяют: 
  
- Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.
    
- Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.
    
- Указывать сообщение, которое будет отображаться пользователям при подписании формы.
    
- Вставлять и просматривать подпись документа. 
    
- Просматривать утверждаемые неотрекаемые сведения, добавленные к каждой подписи для повышения безопасности. Эти дополнительные сведения, которые включают представление формы для каждого подписывающегося лица, являются составным элементом подписи, и их нельзя удалить до тех пор, пока подпись действительна. Эти сведения можно вызвать в любой момент, щелкнув подпись в форме для отображения диалогового окна **Проверка цифровой подписи**. 
    
- Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Обзор объектной модели цифровой подписи

### <a name="the-sign-event"></a>Событие Sign

Объектная модель для цифровых подписей предоставляет следующее событие.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Возникает после выбора для подписания определенного набора данных.  <br/> Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.  <br/> |
   
### <a name="the-signeventargs-object"></a>Объект SignEventArgs

Обработник событий для события [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) может работать с объектом [события SignEventArgs,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) который предоставляет следующие свойства. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Получает набор данных, которые подняли [событие Sign.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx)  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Возвращает или задает факт отображения диалогового окна **Цифровые подписи**.  <br/> |
   
> [!NOTE]
> В модели управляемых [объектов кода Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) отправленной с InfoPath 2003, объект [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) для события [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) предоставляет свойство **XDocument** для доступа к **объекту XDocument** формы, связанной с событием. Это не обязательно с шаблонами форм, созданными с помощью InfoPath Forms Services или InfoPath с помощью [Microsoft.Office. Объектная модель InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) так как к участникам объектной модели класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) можно получить доступ в коде формы с помощью этого **ключевого** слова (C#) или Me **(Visual Basic).** Например, чтобы получить [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) доступ к свойству Подписанный класс [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) чтобы определить, подписана ли форма, можно ввести либо `this.Signed``Me.Signed.`
  
### <a name="collections-and-objects"></a>Семейства и объекты

Объектная модель для цифровых подписей предоставляет следующие семейства.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Коллекция объектов [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в шаблоне формы, как определено во время разработки в режиме проектирования InfoPath.  <br/> Коллекция [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) реализует свойства, которые можно использовать для доступа к объектам [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) связанным с формой. Объект [SignedDataBlockCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) связанный с формой, доступен через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Содержит коллекцию объектов [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) для каждого объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в форме.  <br/> Класс [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) реализует свойства и метод, который можно использовать для доступа к связанным объектам [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) формы и создания подписи. Объект [SignatureCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) связанный с [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) доступен с помощью свойства [Signatures.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx)  <br/> При использовании метода [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) класса [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) имейте в виду, что подпись не будет написана до тех пор, пока метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) не будет вызван на объект [Signature.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) Эти методы можно вызывать только из обработчика событий **Sign** в шаблоне формы с полным доверием.  <br/> |
   
Объектная модель для цифровых подписей предоставляет следующие объекты.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Представляет набор подписываемых данных в форме. Объект [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) предоставляет набор свойств и один метод для программного взаимодействия с набором подписываемых данных.<br/> |
|[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Представляет цифровую подпись, добавленную в форму, или набор подписываемых данных в форме. Объект [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) реализует свойства, которые можно использовать для получения сведений [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) о цифровой подписи, а также метод Sign для написания блока цифровой подписи XML и вычисления его значения криптографического хаши.  <br/> |
|[Сертификат](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Представляет цифровой сертификат X.509, использованный для создания подписи.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Программная работа с цифровыми подписями

Объектная модель [Microsoft.Office. Пространство имен InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет участникам возможность программного взаимодействия с цифровыми подписями. В частности, формы с полным доверием могут добавлять настраиваемые сведения в блок подписи до его утверждения, в соответствии со следующей временной шкалой: 
  
1. Пользователь решает добавить цифровую подпись в форму.
    
2. Отображается **диалоговое окно** Цифровые подписи, пользователь щелкает **Добавить,** а затем выбирает данные для подписи.
    
3. Событие [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) для выбранных данных, представленных объектом [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) поднято, и выполняется метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) коллекции [SignatureCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) 
    
4. Все необязательные настраиваемые действия выполнены.
    
5. Выполняется [метод Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) объекта [Signature.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) 
    
6. Отображается диалоговое окно **Подписать** для ввода имени (или выбора рисунка подписи), выбора сертификата подписи и ввода комментариев. 
    
7. При щелчке кнопки **Подписать** производится добавление подписи в семейство подписей для формы, а неотрекаемые сведения извлекаются и сохраняются вместе с подписью (их можно впоследствии просмотреть, щелкнув **Просмотреть подписанную форму** в диалоговом окне **Цифровые подписи**, а затем щелкнув **Дополнительные сведения, которые будут включены в подпись**).
    
В следующем примере вызывается метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) при подписании выбранных данных и счетчиках подписи со значением timestamp, извлеченным из надежной службы timestamp. 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


