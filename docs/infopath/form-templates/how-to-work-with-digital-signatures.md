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
# <a name="work-with-digital-signatures"></a><span data-ttu-id="8e879-104">Работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="8e879-104">Work with Digital Signatures</span></span>

<span data-ttu-id="8e879-105">Объектная модель [Microsoft.Office. Пространство имен InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет функции для программной работы с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="8e879-105">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides features for working with digital signatures programmatically.</span></span> 
  
## <a name="digital-signature-features"></a><span data-ttu-id="8e879-106">Функции цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="8e879-106">Digital Signature Features</span></span>

<span data-ttu-id="8e879-107">Предоставляемые в InfoPath функции цифровых подписей позволяют:</span><span class="sxs-lookup"><span data-stu-id="8e879-107">The digital signatures features provided by InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="8e879-108">Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="8e879-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="8e879-p101">Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.</span><span class="sxs-lookup"><span data-stu-id="8e879-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="8e879-111">Указывать сообщение, которое будет отображаться пользователям при подписании формы.</span><span class="sxs-lookup"><span data-stu-id="8e879-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="8e879-112">Вставлять и просматривать подпись документа.</span><span class="sxs-lookup"><span data-stu-id="8e879-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="8e879-p102">Просматривать утверждаемые неотрекаемые сведения, добавленные к каждой подписи для повышения безопасности. Эти дополнительные сведения, которые включают представление формы для каждого подписывающегося лица, являются составным элементом подписи, и их нельзя удалить до тех пор, пока подпись действительна. Эти сведения можно вызвать в любой момент, щелкнув подпись в форме для отображения диалогового окна **Проверка цифровой подписи**.</span><span class="sxs-lookup"><span data-stu-id="8e879-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="8e879-p103">Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи. </span><span class="sxs-lookup"><span data-stu-id="8e879-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="8e879-118">Обзор объектной модели цифровой подписи</span><span class="sxs-lookup"><span data-stu-id="8e879-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="the-sign-event"></a><span data-ttu-id="8e879-119">Событие Sign</span><span class="sxs-lookup"><span data-stu-id="8e879-119">The Sign Event</span></span>

<span data-ttu-id="8e879-120">Объектная модель для цифровых подписей предоставляет следующее событие.</span><span class="sxs-lookup"><span data-stu-id="8e879-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="8e879-121">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8e879-121">**Name**</span></span>|<span data-ttu-id="8e879-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e879-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-123">Sign</span><span class="sxs-lookup"><span data-stu-id="8e879-123">Sign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |<span data-ttu-id="8e879-124">Возникает после выбора для подписания определенного набора данных.</span><span class="sxs-lookup"><span data-stu-id="8e879-124">Occurs after a set of data has been selected to sign.</span></span>  <br/> <span data-ttu-id="8e879-p104">Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.</span><span class="sxs-lookup"><span data-stu-id="8e879-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
### <a name="the-signeventargs-object"></a><span data-ttu-id="8e879-128">Объект SignEventArgs</span><span class="sxs-lookup"><span data-stu-id="8e879-128">The SignEventArgs Object</span></span>

<span data-ttu-id="8e879-129">Обработник событий для события [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) может работать с объектом [события SignEventArgs,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) который предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8e879-129">An event handler for the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event can work with the [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) event object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="8e879-130">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8e879-130">**Name**</span></span>|<span data-ttu-id="8e879-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e879-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-132">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="8e879-132">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |<span data-ttu-id="8e879-133">Получает набор данных, которые подняли [событие Sign.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-133">Gets the set of data that raised the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event.</span></span>  <br/> |
|[<span data-ttu-id="8e879-134">SignatureWizard</span><span class="sxs-lookup"><span data-stu-id="8e879-134">SignatureWizard</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |<span data-ttu-id="8e879-135">Возвращает или задает факт отображения диалогового окна **Цифровые подписи**.</span><span class="sxs-lookup"><span data-stu-id="8e879-135">Gets or sets whether to display the **Digital Signatures** dialog box.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8e879-136">В модели управляемых [объектов кода Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) отправленной с InfoPath 2003, объект [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) для события [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) предоставляет свойство **XDocument** для доступа к **объекту XDocument** формы, связанной с событием.</span><span class="sxs-lookup"><span data-stu-id="8e879-136">In the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) managed code object model that shipped with InfoPath 2003, the [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) event object for the [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) event provides an **XDocument** property for accessing the **XDocument** object of the form associated with the event.</span></span> <span data-ttu-id="8e879-137">Это не обязательно с шаблонами форм, созданными с помощью InfoPath Forms Services или InfoPath с помощью [Microsoft.Office. Объектная модель InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) так как к участникам объектной модели класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) можно получить доступ в коде формы с помощью этого **ключевого** слова (C#) или Me **(Visual Basic).**</span><span class="sxs-lookup"><span data-stu-id="8e879-137">This is not necessary with form templates created with InfoPath Forms Services or InfoPath using the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) object model because the object model members of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class can be accessed in form code using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="8e879-138">Например, чтобы получить [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) доступ к свойству Подписанный класс [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) чтобы определить, подписана ли форма, можно ввести либо `this.Signed``Me.Signed.`</span><span class="sxs-lookup"><span data-stu-id="8e879-138">For example, to access the [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class to determine if a form is signed, you can type either  `this.Signed` or  `Me.Signed.`</span></span>
  
### <a name="collections-and-objects"></a><span data-ttu-id="8e879-139">Семейства и объекты</span><span class="sxs-lookup"><span data-stu-id="8e879-139">Collections and Objects</span></span>

<span data-ttu-id="8e879-140">Объектная модель для цифровых подписей предоставляет следующие семейства.</span><span class="sxs-lookup"><span data-stu-id="8e879-140">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="8e879-141">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8e879-141">**Name**</span></span>|<span data-ttu-id="8e879-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e879-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-143">SignedDataBlockCollection</span><span class="sxs-lookup"><span data-stu-id="8e879-143">SignedDataBlockCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |<span data-ttu-id="8e879-144">Коллекция объектов [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в шаблоне формы, как определено во время разработки в режиме проектирования InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8e879-144">The collection of the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects in the form template as defined at design time in InfoPath design mode.</span></span>  <br/> <span data-ttu-id="8e879-145">Коллекция [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) реализует свойства, которые можно использовать для доступа к объектам [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) связанным с формой.</span><span class="sxs-lookup"><span data-stu-id="8e879-145">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) collection implements properties that can be used to access the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects associated with a form.</span></span> <span data-ttu-id="8e879-146">Объект [SignedDataBlockCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) связанный с формой, доступен через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-146">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) object associated with a form is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span>  <br/> |
|[<span data-ttu-id="8e879-147">SignatureCollection</span><span class="sxs-lookup"><span data-stu-id="8e879-147">SignatureCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |<span data-ttu-id="8e879-148">Содержит коллекцию объектов [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) для каждого объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в форме.</span><span class="sxs-lookup"><span data-stu-id="8e879-148">Contains a collection of [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects for each [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object in the form.</span></span>  <br/> <span data-ttu-id="8e879-149">Класс [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) реализует свойства и метод, который можно использовать для доступа к связанным объектам [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) формы и создания подписи.</span><span class="sxs-lookup"><span data-stu-id="8e879-149">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class implements properties and a method that can be used to access a form's associated [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects and to create a signature.</span></span> <span data-ttu-id="8e879-150">Объект [SignatureCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) связанный с [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) доступен с помощью свойства [Signatures.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-150">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) object associated with a [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) is accessible using the [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) property.</span></span>  <br/> <span data-ttu-id="8e879-151">При использовании метода [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) класса [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) имейте в виду, что подпись не будет написана до тех пор, пока метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) не будет вызван на объект [Signature.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-151">When you use the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method is called on the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object.</span></span> <span data-ttu-id="8e879-152">Эти методы можно вызывать только из обработчика событий **Sign** в шаблоне формы с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="8e879-152">These methods can be called only from the **Sign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="8e879-153">Объектная модель для цифровых подписей предоставляет следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="8e879-153">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="8e879-154">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8e879-154">**Name**</span></span>|<span data-ttu-id="8e879-155">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e879-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-156">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="8e879-156">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="8e879-p109">Представляет набор подписываемых данных в форме. Объект [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) предоставляет набор свойств и один метод для программного взаимодействия с набором подписываемых данных.</span><span class="sxs-lookup"><span data-stu-id="8e879-p109">Represents a set of signable data in a form. The [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.  </span></span><br/> |
|[<span data-ttu-id="8e879-159">Подпись</span><span class="sxs-lookup"><span data-stu-id="8e879-159">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="8e879-160">Представляет цифровую подпись, добавленную в форму, или набор подписываемых данных в форме.</span><span class="sxs-lookup"><span data-stu-id="8e879-160">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="8e879-161">Объект [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) реализует свойства, которые можно использовать для получения сведений [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) о цифровой подписи, а также метод Sign для написания блока цифровой подписи XML и вычисления его значения криптографического хаши.</span><span class="sxs-lookup"><span data-stu-id="8e879-161">The [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="8e879-162">Сертификат</span><span class="sxs-lookup"><span data-stu-id="8e879-162">Certificate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |<span data-ttu-id="8e879-163">Представляет цифровой сертификат X.509, использованный для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="8e879-163">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="8e879-164">Программная работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="8e879-164">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="8e879-165">Объектная модель [Microsoft.Office. Пространство имен InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет участникам возможность программного взаимодействия с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="8e879-165">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides members for interacting with digital signatures programmatically.</span></span> <span data-ttu-id="8e879-166">В частности, формы с полным доверием могут добавлять настраиваемые сведения в блок подписи до его утверждения, в соответствии со следующей временной шкалой:</span><span class="sxs-lookup"><span data-stu-id="8e879-166">In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span> 
  
1. <span data-ttu-id="8e879-167">Пользователь решает добавить цифровую подпись в форму.</span><span class="sxs-lookup"><span data-stu-id="8e879-167">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="8e879-168">Отображается **диалоговое окно** Цифровые подписи, пользователь щелкает **Добавить,** а затем выбирает данные для подписи.</span><span class="sxs-lookup"><span data-stu-id="8e879-168">The **Digital Signatures** dialog box is displayed, the user clicks **Add**, and then selects the data to sign.</span></span>
    
3. <span data-ttu-id="8e879-169">Событие [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) для выбранных данных, представленных объектом [SignedDataBlock,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) поднято, и выполняется метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) коллекции [SignatureCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-169">The [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event for the selected data represented by the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object is raised, and the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method of [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object and the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) collection are executed.</span></span> 
    
4. <span data-ttu-id="8e879-170">Все необязательные настраиваемые действия выполнены.</span><span class="sxs-lookup"><span data-stu-id="8e879-170">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="8e879-171">Выполняется [метод Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) объекта [Signature.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e879-171">The [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method of the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object is executed.</span></span> 
    
6. <span data-ttu-id="8e879-172">Отображается диалоговое окно **Подписать** для ввода имени (или выбора рисунка подписи), выбора сертификата подписи и ввода комментариев.</span><span class="sxs-lookup"><span data-stu-id="8e879-172">The **Sign** dialog box is displayed for typing a name (or selecting a signature image), selecting a certificate to sign with, and to enter comments.</span></span> 
    
7. <span data-ttu-id="8e879-173">При щелчке кнопки **Подписать** производится добавление подписи в семейство подписей для формы, а неотрекаемые сведения извлекаются и сохраняются вместе с подписью (их можно впоследствии просмотреть, щелкнув **Просмотреть подписанную форму** в диалоговом окне **Цифровые подписи**, а затем щелкнув **Дополнительные сведения, которые будут включены в подпись**).</span><span class="sxs-lookup"><span data-stu-id="8e879-173">When the **Sign** button is clicked, the signature is added to the collection of signatures for the form and the non-repudiation information is captured and saved with the signature (which can be viewed later by clicking **View Signed Form** on the **Digital Signatures** dialog box, and then clicking **See the additional signing information that was collected**).</span></span>
    
<span data-ttu-id="8e879-174">В следующем примере вызывается метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) при подписании выбранных данных и счетчиках подписи со значением timestamp, извлеченным из надежной службы timestamp.</span><span class="sxs-lookup"><span data-stu-id="8e879-174">The following example invokes the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method when the user signs the selected data and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
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


