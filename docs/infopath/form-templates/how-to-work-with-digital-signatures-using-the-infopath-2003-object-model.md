---
title: Работа с цифровыми подписями с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- цифровые подписи [infopath 2007], шаблоны форм, совместимые с infopath 2003, шаблоны форм, совместимые с InfoPath 2003, цифровые подписи
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Объектная модель, совместимая с InfoPath 2003, предоставляет функции для программной работы с цифровыми подписями.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433446"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Работа с цифровыми подписями с помощью объектной модели InfoPath 2003

Объектная модель, совместимая с InfoPath 2003, предоставляет функции для программной работы с цифровыми подписями.
  
## <a name="digital-signature-features"></a>Возможности цифровой подписи

Доступные в InfoPath функции цифровых подписей позволяют: 
  
- Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.
    
- Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.
    
- Указывать сообщение, которое будет отображаться пользователям при подписании формы.
    
- Вставлять и просматривать подпись документа. 
    
- Просматривать утверждаемые неотрекаемые сведения, добавленные к каждой подписи для повышения безопасности. Эти дополнительные сведения, которые включают представление формы для каждого подписывающегося лица, являются составным элементом подписи, и их нельзя удалить до тех пор, пока подпись действительна. Эти сведения можно вызвать в любой момент, щелкнув подпись в форме для отображения диалогового окна **Проверка цифровой подписи**. 
    
- Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Обзор объектной модели цифровой подписи

### <a name="events"></a>События

Объектная модель для цифровых подписей предоставляет следующее событие.
  
|**Название**|**Описание**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Возникает после выбора для подписания определенного набора подписываемых данных.  <br/> Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.  <br/> |
   
Событие **OnSign** возвращает ссылку на объект [SignEventObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) который предоставляет следующие свойства. 
  
|**Название**|**Описание**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Возвращает или задает значение **Boolean**, указывающее на возвращенное состояние события **OnSign**.  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Возвращает подписанный блок данных, активирующий событие **OnSign**.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Возвращает ссылку на объект **XDocument**, связанный с событием **OnSign**.  <br/> |
   
### <a name="collections-and-objects"></a>Семейства и объекты

Объектная модель для цифровых подписей предоставляет следующие семейства.
  
|**Название**|**Описание**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |Коллекция объектов [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) в шаблоне формы, как определено в файле определения формы (XSF).  <br/> Семейство **SignedDataBlocksCollection** реализует свойства, которые можно использовать для доступа к объектам **SignedDataBlockObjects**, связанным с формой. Коллекция **SignedDataBlocks** доступна через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) объекта [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Содержит коллекцию объектов [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) для каждого **объекта SignedDataBlockObject** в форме.  <br/> Коллекция **SignaturesCollection** реализует свойства и метод, с помощью которых возможен доступ к связанным с формой объектам **SignatureObject**, а также создание подписи. Доступ к семейству предоставляется через объект **SignedDataBlockObject**.  <br/> При использовании метода [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) коллекции **SignaturesCollection** помните, что подпись не написана, пока не будет вызван метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) для объекта **SignatureObject.** Эти методы можно вызвать только из обработчика событий **OnSign** для шаблона формы с полным доверием.  <br/> |
   
Объектная модель для цифровых подписей предоставляет следующие объекты.
  
|**Название**|**Описание**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Представляет набор подписываемых данных в форме. Объект **SignedDataBlock** предоставляет набор свойств и один метод для программного взаимодействия с набором подписываемых данных.  <br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Представляет цифровую подпись, добавленную в форму, или набор подписываемых данных в форме. Коллекция **SignatureObject** реализует свойства, которые можно использовать для получения сведений о цифровой подписи, и метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) для записи блока цифровой подписи XML и вычисления его криптографического значения.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Представляет цифровой сертификат X.509, использованный для создания подписи.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Программная работа с цифровыми подписями

Объектная модель, совместимая с InfoPath 2003, предоставляет элементы для программного взаимодействия с цифровыми подписями. В частности, формы с полным доверием могут добавлять настраиваемые сведения в блок подписи до его применения, в соответствии со следующей временной шкалой:
  
1. Пользователь решает добавить цифровую подпись в форму.
    
2. Отображается первая область **Мастера создания цифровой подписи**. 
    
3. Событие **OnSign** для выбранных данных представляется созданием объекта **SignedDataBlockObject** и выполнением метода **Sign** семейства **SignedDataBlockObject** и метода **Create** семейства **SignaturesCollection**. 
    
4. Все необязательные настраиваемые действия выполнены.
    
5. Метод **Sign** семейства **SignatureObject** выполнен. 
    
6. Отображаются вторая и третья области мастера для выбора сертификата подписи и ввода комментариев.
    
7. Отображаются неотрекаемые сведения (которые можно просмотреть впоследствии с помощью диалогового окна **Проверка цифровой подписи**). 
    
8. При щелчке кнопки **Подписать** производится добавление подписи в семейство подписей для формы. 
    
В следующем примере вызывается диалоговое окно **Подписать**, и подпись визируется значением метки времени, полученной из надежной службы метки времени. 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


