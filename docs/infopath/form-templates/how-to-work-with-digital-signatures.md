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
ms.lasthandoff: 06/21/2018
ms.locfileid: "19807546"
---
# <a name="work-with-digital-signatures"></a><span data-ttu-id="062f8-104">Работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="062f8-104">Work with Digital Signatures</span></span>

<span data-ttu-id="062f8-105">Объектная модель пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет функции для работы с цифровыми подписями программными средствами.</span><span class="sxs-lookup"><span data-stu-id="062f8-105">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides features for working with digital signatures programmatically.</span></span> 
  
## <a name="digital-signature-features"></a><span data-ttu-id="062f8-106">Функции цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="062f8-106">Digital Signature Features</span></span>

<span data-ttu-id="062f8-107">Предоставляемые в InfoPath функции цифровых подписей позволяют: </span><span class="sxs-lookup"><span data-stu-id="062f8-107">The digital signatures features provided by InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="062f8-108">Применять цифровые подписи ко всей форме или к определенным наборам данных в форме, которые можно подписывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="062f8-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="062f8-p101">Указывать каждый набор данных, который можно подписать, а также разрешается ли использовать только одну подпись или возможно использование нескольких подписей с установлением определенных соотношений между ними. Например, можно задать, являются ли все подписи параллельными или каждая подпись отменяет действие предыдущих.</span><span class="sxs-lookup"><span data-stu-id="062f8-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="062f8-111">Указывать сообщение, которое будет отображаться пользователям при подписании формы.</span><span class="sxs-lookup"><span data-stu-id="062f8-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="062f8-112">Вставлять и просматривать подпись документа. </span><span class="sxs-lookup"><span data-stu-id="062f8-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="062f8-113">Просмотр проверяемые неотрекаемые сведения, который был добавлен для каждой подписи для повышения уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="062f8-113">View verifiable non-repudiation information that has been added to each signature for increased security.</span></span> <span data-ttu-id="062f8-114">Дополнительные сведения, которые содержит представление формы, как она представляется каждому подписавшему, входящий в состав подписи и не может быть удалена оставляя подпись.</span><span class="sxs-lookup"><span data-stu-id="062f8-114">This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature.</span></span> <span data-ttu-id="062f8-115">В любое время можно отозвать эти данные, щелкнув подпись в форму, чтобы открыть диалоговое окно **Проверка цифровой подписи** .</span><span class="sxs-lookup"><span data-stu-id="062f8-115">At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="062f8-p103">Пользоваться преимуществами объектной модели для работы с цифровыми подписями. Добавляйте настраиваемые сведения в блок подписи форм с полным доверием, используя объектную модель цифровой подписи. </span><span class="sxs-lookup"><span data-stu-id="062f8-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="062f8-118">Обзор объектной модели цифровой подписи</span><span class="sxs-lookup"><span data-stu-id="062f8-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="the-sign-event"></a><span data-ttu-id="062f8-119">Событие Sign</span><span class="sxs-lookup"><span data-stu-id="062f8-119">The Sign Event</span></span>

<span data-ttu-id="062f8-120">Объектная модель для цифровых подписей предоставляет следующее событие.</span><span class="sxs-lookup"><span data-stu-id="062f8-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="062f8-121">**Имя**</span><span class="sxs-lookup"><span data-stu-id="062f8-121">**Name**</span></span>|<span data-ttu-id="062f8-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="062f8-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="062f8-123">Знак</span><span class="sxs-lookup"><span data-stu-id="062f8-123">Sign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |<span data-ttu-id="062f8-124">Возникает после выбора для подписания определенного набора данных.</span><span class="sxs-lookup"><span data-stu-id="062f8-124">Occurs after a set of data has been selected to sign.</span></span>  <br/> <span data-ttu-id="062f8-p104">Это событие можно использовать для управления данными, хранящимися внутри цифровой подписи. Например, можно добавить данные с надежного сервера метки времени или добавить серверную подпись других сторон для транзакции. Также можно использовать это событие для блокирования подписания, если текущий пользователь не входит в состав определенной группы.</span><span class="sxs-lookup"><span data-stu-id="062f8-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
### <a name="the-signeventargs-object"></a><span data-ttu-id="062f8-128">Объект SignEventArgs</span><span class="sxs-lookup"><span data-stu-id="062f8-128">The SignEventArgs Object</span></span>

<span data-ttu-id="062f8-129">Обработчик событий для события [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) может работать с объектом событий [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , который предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="062f8-129">An event handler for the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event can work with the [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) event object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="062f8-130">**Имя**</span><span class="sxs-lookup"><span data-stu-id="062f8-130">**Name**</span></span>|<span data-ttu-id="062f8-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="062f8-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="062f8-132">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="062f8-132">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |<span data-ttu-id="062f8-133">Получает набор данных, который вызвал событие [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) .</span><span class="sxs-lookup"><span data-stu-id="062f8-133">Gets the set of data that raised the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event.</span></span>  <br/> |
|[<span data-ttu-id="062f8-134">SignatureWizard</span><span class="sxs-lookup"><span data-stu-id="062f8-134">SignatureWizard</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |<span data-ttu-id="062f8-135">Получает или задает факт отображения диалогового окна **Цифровые подписи** .</span><span class="sxs-lookup"><span data-stu-id="062f8-135">Gets or sets whether to display the **Digital Signatures** dialog box.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="062f8-136">В управляемом коде объектной модели [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , поставляемый с InfoPath 2003 объект [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) события для события [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) предоставляет свойство **XDocument** для доступа к ** XDocument** объекта формы, связанный с событием.</span><span class="sxs-lookup"><span data-stu-id="062f8-136">In the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) managed code object model that shipped with InfoPath 2003, the [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) event object for the [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) event provides an **XDocument** property for accessing the **XDocument** object of the form associated with the event.</span></span> <span data-ttu-id="062f8-137">Это не требуется с шаблонами форм, созданных с помощью службы InfoPath Forms Services или с помощью объектной модели [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , так как элементы объектной модели класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) может осуществляться в код формы с помощью **это InfoPath **(C#) или ключевое слово **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="062f8-137">This is not necessary with form templates created with InfoPath Forms Services or InfoPath using the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) object model because the object model members of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class can be accessed in form code using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="062f8-138">Например, для доступа к свойству [выполнен вход](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , чтобы определить, если подпись формы, можно ввести либо `this.Signed` или`Me.Signed.`</span><span class="sxs-lookup"><span data-stu-id="062f8-138">For example, to access the [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class to determine if a form is signed, you can type either  `this.Signed` or  `Me.Signed.`</span></span>
  
### <a name="collections-and-objects"></a><span data-ttu-id="062f8-139">Семейства и объекты</span><span class="sxs-lookup"><span data-stu-id="062f8-139">Collections and Objects</span></span>

<span data-ttu-id="062f8-140">Объектная модель для цифровых подписей предоставляет следующие семейства.</span><span class="sxs-lookup"><span data-stu-id="062f8-140">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="062f8-141">**Имя**</span><span class="sxs-lookup"><span data-stu-id="062f8-141">**Name**</span></span>|<span data-ttu-id="062f8-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="062f8-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="062f8-143">SignedDataBlockCollection</span><span class="sxs-lookup"><span data-stu-id="062f8-143">SignedDataBlockCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |<span data-ttu-id="062f8-144">Коллекция объектов [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в шаблоне формы, заданных во время разработки в режиме конструктора InfoPath.</span><span class="sxs-lookup"><span data-stu-id="062f8-144">The collection of the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects in the form template as defined at design time in InfoPath design mode.</span></span>  <br/> <span data-ttu-id="062f8-145">Коллекция [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) реализует свойства, которые можно использовать для доступа к объектам [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) , связанный с формой.</span><span class="sxs-lookup"><span data-stu-id="062f8-145">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) collection implements properties that can be used to access the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects associated with a form.</span></span> <span data-ttu-id="062f8-146">Объект [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , связанный с формой доступен через свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="062f8-146">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) object associated with a form is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span>  <br/> |
|[<span data-ttu-id="062f8-147">SignatureCollection</span><span class="sxs-lookup"><span data-stu-id="062f8-147">SignatureCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |<span data-ttu-id="062f8-148">Содержит коллекцию объектов [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) для каждого объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) в форме.</span><span class="sxs-lookup"><span data-stu-id="062f8-148">Contains a collection of [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects for each [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object in the form.</span></span>  <br/> <span data-ttu-id="062f8-149">Класс [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) реализует свойства и метод, который может использоваться для доступа к связанным объектам [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) формы и для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="062f8-149">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class implements properties and a method that can be used to access a form's associated [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects and to create a signature.</span></span> <span data-ttu-id="062f8-150">Объект [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , связанный с [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) доступен с помощью свойства [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .</span><span class="sxs-lookup"><span data-stu-id="062f8-150">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) object associated with a [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) is accessible using the [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) property.</span></span>  <br/> <span data-ttu-id="062f8-151">При использовании метода [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) класса [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) помните, что до [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) не записывается подписи для объекта [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="062f8-151">When you use the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method is called on the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object.</span></span> <span data-ttu-id="062f8-152">Эти методы могут вызываться только из обработчика событий **входа** шаблона полностью доверенной формы.</span><span class="sxs-lookup"><span data-stu-id="062f8-152">These methods can be called only from the **Sign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="062f8-153">Объектная модель для цифровых подписей предоставляет следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="062f8-153">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="062f8-154">**Имя**</span><span class="sxs-lookup"><span data-stu-id="062f8-154">**Name**</span></span>|<span data-ttu-id="062f8-155">**Описание**</span><span class="sxs-lookup"><span data-stu-id="062f8-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="062f8-156">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="062f8-156">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="062f8-157">Представляет набор подписываемых данных в форме.</span><span class="sxs-lookup"><span data-stu-id="062f8-157">Represents a set of signable data in a form.</span></span> <span data-ttu-id="062f8-158">Объект [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) предоставляет ряд свойств и один метод, который можно использовать для программного взаимодействия с набор подписываемых данных.</span><span class="sxs-lookup"><span data-stu-id="062f8-158">The [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.</span></span>  <br/> |
|[<span data-ttu-id="062f8-159">Подпись</span><span class="sxs-lookup"><span data-stu-id="062f8-159">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="062f8-160">Представляет цифровую подпись, добавленную в форму или набор подписываемых данных в форме.</span><span class="sxs-lookup"><span data-stu-id="062f8-160">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="062f8-161">Объект [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) реализует свойства, которые можно использовать для получения сведений о цифровой подписи и метод [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) запись блока цифровой подписи XML и вычислений криптографический хэш.</span><span class="sxs-lookup"><span data-stu-id="062f8-161">The [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="062f8-162">Сертификат</span><span class="sxs-lookup"><span data-stu-id="062f8-162">Certificate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |<span data-ttu-id="062f8-163">Представляет цифровой сертификат X.509, использованный для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="062f8-163">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="062f8-164">Программная работа с цифровыми подписями</span><span class="sxs-lookup"><span data-stu-id="062f8-164">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="062f8-165">Объектная модель пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) предоставляет члены для программного взаимодействия с цифровыми подписями.</span><span class="sxs-lookup"><span data-stu-id="062f8-165">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides members for interacting with digital signatures programmatically.</span></span> <span data-ttu-id="062f8-166">В частности полностью доверенных форм можно добавить различные сведения в блок подписи перед сохранением, согласно следующей шкале:</span><span class="sxs-lookup"><span data-stu-id="062f8-166">In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span> 
  
1. <span data-ttu-id="062f8-167">Пользователь решает добавить цифровую подпись в форму.</span><span class="sxs-lookup"><span data-stu-id="062f8-167">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="062f8-168">Отображается диалоговое окно **Цифровые подписи** , пользователь щелкает **Добавить**, а затем выбирает данные для входа.</span><span class="sxs-lookup"><span data-stu-id="062f8-168">The **Digital Signatures** dialog box is displayed, the user clicks **Add**, and then selects the data to sign.</span></span>
    
3. <span data-ttu-id="062f8-169">Возникает событие [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) для выбранных данных, представленного объектом [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) объекта [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) и метод [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) выполняются семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="062f8-169">The [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event for the selected data represented by the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object is raised, and the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method of [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object and the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) collection are executed.</span></span> 
    
4. <span data-ttu-id="062f8-170">Все необязательные настраиваемые действия выполнены.</span><span class="sxs-lookup"><span data-stu-id="062f8-170">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="062f8-171">Выполняет метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) объекта [подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) .</span><span class="sxs-lookup"><span data-stu-id="062f8-171">The [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method of the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object is executed.</span></span> 
    
6. <span data-ttu-id="062f8-172">Откроется диалоговое окно **входа** для ввода имени (или выбора рисунка подписи), выбора сертификата подписи и ввода комментариев.</span><span class="sxs-lookup"><span data-stu-id="062f8-172">The **Sign** dialog box is displayed for typing a name (or selecting a signature image), selecting a certificate to sign with, and to enter comments.</span></span> 
    
7. <span data-ttu-id="062f8-173">При щелчке кнопки **подписать** производится добавление подписи в семейство подписей для формы и захватываются и сохраняются с подписью (который можно просмотреть впоследствии, нажав кнопку **Просмотреть подписанную форму** на **неотрекаемые сведения Цифровые подписи** диалоговое окно, а затем нажав кнопку **просмотреть дополнительные сведения о подписи, собранных**).</span><span class="sxs-lookup"><span data-stu-id="062f8-173">When the **Sign** button is clicked, the signature is added to the collection of signatures for the form and the non-repudiation information is captured and saved with the signature (which can be viewed later by clicking **View Signed Form** on the **Digital Signatures** dialog box, and then clicking **See the additional signing information that was collected**).</span></span>
    
<span data-ttu-id="062f8-174">В следующем примере вызывается метод [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) , когда пользователь подписывает выбранные данные и визирует подпись значением метки времени извлекается из надежной службы метки времени.</span><span class="sxs-lookup"><span data-stu-id="062f8-174">The following example invokes the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method when the user signs the selected data and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
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


