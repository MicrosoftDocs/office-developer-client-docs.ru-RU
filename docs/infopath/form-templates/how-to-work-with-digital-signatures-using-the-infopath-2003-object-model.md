---
title: Работать с цифровыми подписями с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Цифровые подписи [InfoPath 2007], шаблоны форм, совместимые с InfoPath 2003, шаблоны форм, совместимые с InfoPath 2003, цифровые подписи
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
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a><span data-ttu-id="e8228-104">Работать с цифровыми подписями с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="e8228-104">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="e8228-105">Объектная модель, совместимая с InfoPath 2003, предоставляет функции для программной работы с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="e8228-105">The InfoPath 2003-compatible object model provides features for working with digital signatures programmatically.</span></span>
  
## <a name="digital-signature-features"></a><span data-ttu-id="e8228-106">Возможности цифровой подписи</span><span class="sxs-lookup"><span data-stu-id="e8228-106">Digital Signature Features</span></span>

<span data-ttu-id="e8228-107">Доступные в InfoPath функции цифровых подписей позволяют:</span><span class="sxs-lookup"><span data-stu-id="e8228-107">The digital signatures features available in InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="e8228-108">Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="e8228-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="e8228-p101">Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.</span><span class="sxs-lookup"><span data-stu-id="e8228-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="e8228-111">Указывать сообщение, которое будет отображаться пользователям при подписании формы.</span><span class="sxs-lookup"><span data-stu-id="e8228-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="e8228-112">Вставлять и просматривать подпись документа.</span><span class="sxs-lookup"><span data-stu-id="e8228-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="e8228-p102">Просматривать утверждаемые неотрекаемые сведения, добавленные к каждой подписи для повышения безопасности. Эти дополнительные сведения, которые включают представление формы для каждого подписывающегося лица, являются составным элементом подписи, и их нельзя удалить до тех пор, пока подпись действительна. Эти сведения можно вызвать в любой момент, щелкнув подпись в форме для отображения диалогового окна **Проверка цифровой подписи**.</span><span class="sxs-lookup"><span data-stu-id="e8228-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="e8228-p103">Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи. </span><span class="sxs-lookup"><span data-stu-id="e8228-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="e8228-118">Обзор объектной модели цифровой подписи</span><span class="sxs-lookup"><span data-stu-id="e8228-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="events"></a><span data-ttu-id="e8228-119">События</span><span class="sxs-lookup"><span data-stu-id="e8228-119">Events</span></span>

<span data-ttu-id="e8228-120">Объектная модель для цифровых подписей предоставляет следующее событие.</span><span class="sxs-lookup"><span data-stu-id="e8228-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="e8228-121">**Название**</span><span class="sxs-lookup"><span data-stu-id="e8228-121">**Name**</span></span>|<span data-ttu-id="e8228-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8228-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8228-123">OnSign</span><span class="sxs-lookup"><span data-stu-id="e8228-123">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="e8228-124">Возникает после выбора для подписания определенного набора подписываемых данных.</span><span class="sxs-lookup"><span data-stu-id="e8228-124">Occurs after a set of signable data has been selected to sign.</span></span>  <br/> <span data-ttu-id="e8228-p104">Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.</span><span class="sxs-lookup"><span data-stu-id="e8228-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
<span data-ttu-id="e8228-128">Событие **OnSign** возвращает ссылку на объект [сигневентобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , который предоставляет указанные ниже свойства.</span><span class="sxs-lookup"><span data-stu-id="e8228-128">The **OnSign** event returns a reference to the [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="e8228-129">**Название**</span><span class="sxs-lookup"><span data-stu-id="e8228-129">**Name**</span></span>|<span data-ttu-id="e8228-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8228-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8228-131">ReturnStatus</span><span class="sxs-lookup"><span data-stu-id="e8228-131">ReturnStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |<span data-ttu-id="e8228-132">Возвращает или задает значение **Boolean**, указывающее на возвращенное состояние события **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="e8228-132">Gets or sets a **Boolean** value indicating the return status of the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="e8228-133">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="e8228-133">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |<span data-ttu-id="e8228-134">Возвращает подписанный блок данных, активирующий событие **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="e8228-134">Gets the signed data block that triggered the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="e8228-135">XDocument</span><span class="sxs-lookup"><span data-stu-id="e8228-135">XDocument</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |<span data-ttu-id="e8228-136">Возвращает ссылку на объект **XDocument**, связанный с событием **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="e8228-136">Gets a reference to the **XDocument** object associated with the **OnSign** event.</span></span>  <br/> |
   
### <a name="collections-and-objects"></a><span data-ttu-id="e8228-137">Семейства и объекты</span><span class="sxs-lookup"><span data-stu-id="e8228-137">Collections and Objects</span></span>

<span data-ttu-id="e8228-138">Объектная модель для цифровых подписей предоставляет следующие семейства.</span><span class="sxs-lookup"><span data-stu-id="e8228-138">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="e8228-139">**Название**</span><span class="sxs-lookup"><span data-stu-id="e8228-139">**Name**</span></span>|<span data-ttu-id="e8228-140">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8228-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8228-141">сигнеддатаблокксколлектион</span><span class="sxs-lookup"><span data-stu-id="e8228-141">SignedDataBlocksCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |<span data-ttu-id="e8228-142">Коллекция объектов [сигнеддатаблоккобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) в шаблоне формы, как определено в файле определения формы (XSF).</span><span class="sxs-lookup"><span data-stu-id="e8228-142">The collection of the [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) objects in the form template as defined in the form definition file (.xsf).</span></span>  <br/> <span data-ttu-id="e8228-143">Семейство **SignedDataBlocksCollection** реализует свойства, которые можно использовать для доступа к объектам **SignedDataBlockObjects**, связанным с формой.</span><span class="sxs-lookup"><span data-stu-id="e8228-143">The **SignedDataBlocksCollection** collection implements properties that can be used to access the **SignedDataBlockObjects** objects associated with a form.</span></span> <span data-ttu-id="e8228-144">Коллекция **сигнеддатаблоккс** доступна через свойство [сигнеддатаблоккс](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) объекта [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e8228-144">The **SignedDataBlocks** collection is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) object.</span></span>  <br/> |
|[<span data-ttu-id="e8228-145">сигнатуресколлектион</span><span class="sxs-lookup"><span data-stu-id="e8228-145">SignaturesCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |<span data-ttu-id="e8228-146">Содержит коллекцию объектов [сигнатуреобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) для каждого **сигнеддатаблоккобжект** в форме.</span><span class="sxs-lookup"><span data-stu-id="e8228-146">Contains a collection of [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objects for each **SignedDataBlockObject** in the form.</span></span>  <br/> <span data-ttu-id="e8228-147">Коллекция **SignaturesCollection** реализует свойства и метод, с помощью которых возможен доступ к связанным с формой объектам **SignatureObject**, а также создание подписи.</span><span class="sxs-lookup"><span data-stu-id="e8228-147">The **SignaturesCollection** collection implements properties and a method that can be used to access a form's associated **SignatureObject** objects and to create a signature.</span></span> <span data-ttu-id="e8228-148">Доступ к семейству предоставляется через объект **SignedDataBlockObject**.</span><span class="sxs-lookup"><span data-stu-id="e8228-148">It is accessible through the **SignedDataBlockObject** object.</span></span>  <br/> <span data-ttu-id="e8228-149">При использовании метода [CREATE](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) коллекции **сигнатуресколлектион** следует учитывать, что подпись не записывается, пока не будет вызван метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) для объекта **сигнатуреобжект** .</span><span class="sxs-lookup"><span data-stu-id="e8228-149">When you use the [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) method of the **SignaturesCollection** collection, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method is called on the **SignatureObject** object.</span></span> <span data-ttu-id="e8228-150">Эти методы можно вызвать только из обработчика событий **OnSign** для шаблона формы с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="e8228-150">These methods can be called only from the **OnSign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="e8228-151">Объектная модель для цифровых подписей предоставляет следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="e8228-151">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="e8228-152">**Название**</span><span class="sxs-lookup"><span data-stu-id="e8228-152">**Name**</span></span>|<span data-ttu-id="e8228-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8228-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8228-154">сигнеддатаблоккобжект</span><span class="sxs-lookup"><span data-stu-id="e8228-154">SignedDataBlockObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |<span data-ttu-id="e8228-155">Представляет набор подписываемых данных в форме.</span><span class="sxs-lookup"><span data-stu-id="e8228-155">Represents a set of signable data in a form.</span></span> <span data-ttu-id="e8228-156">Объект **SignedDataBlock** предоставляет набор свойств и один метод для программного взаимодействия с набором подписываемых данных.</span><span class="sxs-lookup"><span data-stu-id="e8228-156">The **SignedDataBlock** object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.</span></span>  <br/> |
|[<span data-ttu-id="e8228-157">сигнатуреобжект</span><span class="sxs-lookup"><span data-stu-id="e8228-157">SignatureObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |<span data-ttu-id="e8228-158">Представляет цифровую подпись, добавленную в форму, или набор подписываемых данных в форме.</span><span class="sxs-lookup"><span data-stu-id="e8228-158">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="e8228-159">Коллекция **сигнатуреобжект** реализует свойства, которые можно использовать для получения сведений о цифровой подписи, а также метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) для записи блока цифровой подписи XML и вычисления его криптографического хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="e8228-159">The **SignatureObject** collection implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="e8228-160">цертификатеобжект</span><span class="sxs-lookup"><span data-stu-id="e8228-160">CertificateObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |<span data-ttu-id="e8228-161">Представляет цифровой сертификат X.509, использованный для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="e8228-161">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="e8228-162">Программная работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="e8228-162">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="e8228-p110">Объектная модель, совместимая с InfoPath 2003, предоставляет элементы для программного взаимодействия с цифровыми подписями. В частности, формы с полным доверием могут добавлять настраиваемые сведения в блок подписи до его применения, в соответствии со следующей временной шкалой:</span><span class="sxs-lookup"><span data-stu-id="e8228-p110">The InfoPath 2003-compatible object model provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span>
  
1. <span data-ttu-id="e8228-165">Пользователь решает добавить цифровую подпись в форму.</span><span class="sxs-lookup"><span data-stu-id="e8228-165">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="e8228-166">Отображается первая область **Мастера создания цифровой подписи**.</span><span class="sxs-lookup"><span data-stu-id="e8228-166">The first panel of the **Digital Signature Wizard** is displayed.</span></span> 
    
3. <span data-ttu-id="e8228-167">Событие **OnSign** для выбранных данных представляется созданием объекта **SignedDataBlockObject** и выполнением метода **Sign** семейства **SignedDataBlockObject** и метода **Create** семейства **SignaturesCollection**.</span><span class="sxs-lookup"><span data-stu-id="e8228-167">The **OnSign** event for the selected data represented by the **SignedDataBlockObject** object is raised, and the **Sign** method of **SignedDataBlockObject** and the **Create** method of the **SignaturesCollection** collection are executed.</span></span> 
    
4. <span data-ttu-id="e8228-168">Все необязательные настраиваемые действия выполнены.</span><span class="sxs-lookup"><span data-stu-id="e8228-168">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="e8228-169">Метод **Sign** семейства **SignatureObject** выполнен.</span><span class="sxs-lookup"><span data-stu-id="e8228-169">The **Sign** method of the **SignatureObject** is executed.</span></span> 
    
6. <span data-ttu-id="e8228-170">Отображаются вторая и третья области мастера для выбора сертификата подписи и ввода комментариев.</span><span class="sxs-lookup"><span data-stu-id="e8228-170">Second and third panes of the wizard are displayed for selecting a certificate to sign with and to enter comments.</span></span>
    
7. <span data-ttu-id="e8228-171">Отображаются неотрекаемые сведения (которые можно просмотреть впоследствии с помощью диалогового окна **Проверка цифровой подписи**).</span><span class="sxs-lookup"><span data-stu-id="e8228-171">The non-repudiation information is displayed (which can be viewed later with the **Verify Digital Signature** dialog box).</span></span> 
    
8. <span data-ttu-id="e8228-172">При щелчке кнопки **Подписать** производится добавление подписи в семейство подписей для формы.</span><span class="sxs-lookup"><span data-stu-id="e8228-172">When the **Sign** button is clicked, the signature is added to collection of signatures for the form.</span></span> 
    
<span data-ttu-id="e8228-173">В следующем примере вызывается диалоговое окно **Подписать**, и подпись визируется значением метки времени, полученной из надежной службы метки времени.</span><span class="sxs-lookup"><span data-stu-id="e8228-173">The following example invokes the **Sign** dialog box and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
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


