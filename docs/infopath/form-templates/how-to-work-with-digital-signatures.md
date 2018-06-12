---
title: Работа с цифровыми подписями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- цифровые подписи [infopath 2007] InfoPath 2007 цифровых подписей
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Объектная модель пространства имен Microsoft.Office.InfoPath предоставляет функции для работы с цифровыми подписями программными средствами.
ms.openlocfilehash: 1277998edf4feb94da40d82372fd4d96fedf2d54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807546"
---
# <a name="work-with-digital-signatures"></a>Работа с цифровыми подписями

Объектная модель пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет функции для работы с цифровыми подписями программными средствами. 
  
## <a name="digital-signature-features"></a>Функции цифровых подписей

Предоставляемые в InfoPath функции цифровых подписей позволяют:  
  
- Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.
    
- Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.
    
- Указывать сообщение, которое будет отображаться пользователям при подписании формы.
    
- Вставлять и просматривать подпись документа.  
    
- Просмотр проверяемые неотрекаемые сведения, который был добавлен для каждой подписи для повышения уровня безопасности. Дополнительные сведения, которые содержит представление формы, как она представляется каждому подписавшему, входящий в состав подписи и не может быть удалена оставляя подпись. В любое время можно отозвать эти данные, щелкнув подпись в форму, чтобы открыть диалоговое окно **Проверка цифровой подписи** . 
    
- Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Обзор объектной модели цифровой подписи

### <a name="the-sign-event"></a>Событие Sign

Объектная модель для цифровых подписей предоставляет следующее событие.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Знак](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Возникает после выбора для подписания определенного набора данных.  <br/> Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.  <br/> |
   
### <a name="the-signeventargs-object"></a>Объект SignEventArgs

Обработчик событий для события [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) может работать с объектом событий [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , который предоставляет следующие свойства. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Получает набор данных, который вызвал событие [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) .  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Получает или задает факт отображения диалогового окна **Цифровые подписи** .  <br/> |
   
> [!NOTE]
> В управляемом коде объектной модели [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , поставляемый с InfoPath 2003 объект [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) события для события [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) предоставляет свойство **XDocument** для доступа к ** XDocument** объекта формы, связанный с событием. Это не требуется с шаблонами форм, созданных с помощью службы InfoPath Forms Services или с помощью объектной модели [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , так как элементы объектной модели класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) может осуществляться в код формы с помощью **это InfoPath **(C#) или ключевое слово **Me** (Visual Basic). Например, для доступа к свойству [выполнен вход](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , чтобы определить, если подпись формы, можно ввести либо `this.Signed` или`Me.Signed.`
  
### <a name="collections-and-objects"></a>Семейства и объекты

Объектная модель для цифровых подписей предоставляет следующие семейства.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Коллекция объектов [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в шаблоне формы, заданных во время разработки в режиме конструктора InfoPath.  <br/> Коллекция [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) реализует свойства, которые можно использовать для доступа к объектам [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) , связанный с формой. Объект [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , связанный с формой доступен через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Содержит коллекцию объектов [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) для каждого объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в форме.  <br/> Класс [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) реализует свойства и метод, который может использоваться для доступа к связанным объектам [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) формы и для создания подписи. Объект [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , связанный с [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) доступен с помощью свойства [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .  <br/> При использовании метода [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) класса [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) помните, что до [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) не записывается подписи для объекта [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) вызывается метод. Эти методы могут вызываться только из обработчика событий **входа** шаблона полностью доверенной формы.  <br/> |
   
Объектная модель для цифровых подписей предоставляет следующие объекты.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Представляет набор подписываемых данных в форме. Объект [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) предоставляет ряд свойств и один метод, который можно использовать для программного взаимодействия с набор подписываемых данных.  <br/> |
|[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Представляет цифровую подпись, добавленную в форму или набор подписываемых данных в форме. Объект [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) реализует свойства, которые можно использовать для получения сведений о цифровой подписи и метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) запись блока цифровой подписи XML и вычислений криптографический хэш.  <br/> |
|[Сертификат](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Представляет цифровой сертификат X.509, использованный для создания подписи.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Программная работа с цифровыми подписями

Объектная модель пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет члены для программного взаимодействия с цифровыми подписями. В частности полностью доверенных форм можно добавить различные сведения в блок подписи перед сохранением, согласно следующей шкале: 
  
1. Пользователь решает добавить цифровую подпись в форму.
    
2. Отображается диалоговое окно **Цифровые подписи** , пользователь щелкает **Добавить**, а затем выбирает данные для входа.
    
3. Возникает событие [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) для выбранных данных, представленного объектом [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) выполняются семейства сайтов. 
    
4. Все необязательные настраиваемые действия выполнены.
    
5. Выполняет метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) объекта [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . 
    
6. Откроется диалоговое окно **входа** для ввода имени (или выбора рисунка подписи), выбора сертификата подписи и ввода комментариев. 
    
7. При щелчке кнопки **подписать** производится добавление подписи в семейство подписей для формы и захватываются и сохраняются с подписью (который можно просмотреть впоследствии, нажав кнопку **Просмотреть подписанную форму** на **неотрекаемые сведения Цифровые подписи** диалоговое окно, а затем нажав кнопку **просмотреть дополнительные сведения о подписи, собранных**).
    
В следующем примере вызывается метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) , когда пользователь подписывает выбранные данные и визирует подпись значением метки времени извлекается из надежной службы метки времени. 
  
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


