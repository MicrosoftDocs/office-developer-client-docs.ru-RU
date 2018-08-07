---
title: Работа с цифровыми подписями при помощи объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- цифровые подписи [infopath 2007], шаблоны форм с поддержкой 2003 infopath, совместимых с InfoPath 2003 шаблонов форм, цифровые подписи
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Объектная модель, совместимая с InfoPath 2003, предоставляет функции для программной работы с цифровыми подписями.
ms.openlocfilehash: ae9934e36766b7e783d1404a12a49e9b0b08543a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807511"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Работа с цифровыми подписями при помощи объектной модели InfoPath 2003

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
  
|**Имя**|**Описание**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Возникает после выбора для подписания определенного набора подписываемых данных.  <br/> Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.  <br/> |
   
Событие **OnSign** возвращает ссылку на объект [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , который предоставляет следующие свойства. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Возвращает или задает значение **Boolean**, указывающее на возвращенное состояние события **OnSign**.  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Возвращает подписанный блок данных, активирующий событие **OnSign**.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Возвращает ссылку на объект **XDocument**, связанный с событием **OnSign**.  <br/> |
   
### <a name="collections-and-objects"></a>Семейства и объекты

Объектная модель для цифровых подписей предоставляет следующие семейства.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |Коллекция объектов [объекта SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) в шаблоне формы, определенные в файле определения формы (XSF).  <br/> Коллекция **SignedDataBlocksCollection** реализует свойства, которые можно использовать для доступа к объектам **SignedDataBlockObjects** , связанный с формой. Коллекция **SignedDataBlocks** доступен через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) объекта [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Содержит коллекцию объектов [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) для каждого **объекта SignedDataBlockObject** в форме.  <br/> Семейство **SignaturesCollection** реализует свойства и метод, которые можно использовать для доступа к связанным с формой объектам **SignatureObject**, а также для создания подписи. Доступ к семейству предоставляется через объект **SignedDataBlockObject**. <br/> При использовании метода [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) семействе **SignaturesCollection** помните, что подпись не записывается до [входа](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) вызывается метод на объект **SignatureObject** . Эти методы могут вызываться только из обработчика события **OnSign** шаблона полностью доверенной формы.  <br/> |
   
Объектная модель для цифровых подписей предоставляет следующие объекты.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Объекта SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Представляет набор подписываемых данных в форме. Объект **SignedDataBlock** предоставляет набор свойств и один метод для программного взаимодействия с набором подписываемых данных.<br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Представляет цифровую подпись, добавленную в форму или набор подписываемых данных в форме. Семейства **SignatureObject** реализует свойства, которые можно использовать для получения сведений о цифровой подписи и метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) запись блока цифровой подписи XML и вычислений криптографический хэш.  <br/> |
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


