---
title: Поддержка Office для Android для платформы Android Storage Access Framework
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office для Android интегрируется с платформой Android Storage Access Framework, которая позволяет Office открывать файлы, хранимые другим поставщиком документов.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300352"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="c5109-103">Поддержка Office для Android для платформы Android Storage Access Framework</span><span class="sxs-lookup"><span data-stu-id="c5109-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="c5109-104">Office для Android интегрируется с платформой Android Storage Access Framework, которая позволяет Office открывать файлы, хранимые другим поставщиком документов.</span><span class="sxs-lookup"><span data-stu-id="c5109-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="c5109-p101">Android 4.4 (API уровня 19) представляет платформу Storage Access Framework (SAF). SAF позволяет пользователям просматривать и открывать документы, изображения и другие файлы всех поставщиков хранилищ документов, которые предпочитают пользователи. Стандартный пользовательский интерфейс позволяет просматривать файлы и получать доступ к ним подходящим способом по всем приложениям и поставщикам.</span><span class="sxs-lookup"><span data-stu-id="c5109-p101">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF). The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers. A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="c5109-108">Реализация поставщика документа</span><span class="sxs-lookup"><span data-stu-id="c5109-108">Implement a document provider</span></span>

<span data-ttu-id="c5109-p102">Если вы разрабатываете приложение, предоставляющее службы хранения для документов, вы можете предоставить доступ к файлам через платформу SAF, [записав поставщика пользовательских документов](https://developer.android.com/guide/topics/providers/document-provider.html). Затем приложения Office могут вызвать намерение [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) и/или [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html). чтобы получить файлы, возвращенные поставщиком документов. Обратите внимание, что намерение может включать фильтры для дальнейшего уточнения критериев.</span><span class="sxs-lookup"><span data-stu-id="c5109-p102">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html). Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider. Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="c5109-112">Включение бесплатных правок для пользователей</span><span class="sxs-lookup"><span data-stu-id="c5109-112">Enable free consumer edits</span></span>

<span data-ttu-id="c5109-p103">Пользователи могут входить в приложения Office с помощью бесплатной учетной записи Майкрософт, чтобы создавать или редактировать документы, хранящиеся в службе хранения, ориентированной на пользователя. В следующей таблице перечислены обязательные свойства, которые поставщики обязаны поставлять как часть курсора, чтобы позволить пользователям бесплатно редактировать документы, доступные через платформу Storage Access Framework.</span><span class="sxs-lookup"><span data-stu-id="c5109-p103">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service. The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="c5109-115">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="c5109-115">**Property**</span></span>|<span data-ttu-id="c5109-116">**Индекс**</span><span class="sxs-lookup"><span data-stu-id="c5109-116">**Index**</span></span>|<span data-ttu-id="c5109-117">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c5109-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5109-118">Тип документа</span><span class="sxs-lookup"><span data-stu-id="c5109-118">Document Type</span></span>  <br/> |<span data-ttu-id="c5109-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="c5109-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="c5109-120">\<consumer\></span><span class="sxs-lookup"><span data-stu-id="c5109-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="c5109-121">Понятное имя службы</span><span class="sxs-lookup"><span data-stu-id="c5109-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="c5109-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="c5109-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="c5109-p104">Любое понятное для пользователей имя службы, используемое для определения документа в списке недавно использовавшихся документов в приложениях Office. Обратите внимание, что свойство "Условия соглашения" должно быть предоставлено до того, как будет отображено понятное имя службы.</span><span class="sxs-lookup"><span data-stu-id="c5109-p104">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps. Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="c5109-125">Условия соглашения</span><span class="sxs-lookup"><span data-stu-id="c5109-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="c5109-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="c5109-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="c5109-127">\<Я соглашаюсь с условиями, указанными на странице https://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="c5109-127">\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5109-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c5109-128">See also</span></span>
<span data-ttu-id="c5109-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c5109-129"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="c5109-130">Интеграция с Office</span><span class="sxs-lookup"><span data-stu-id="c5109-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="c5109-131">Основные сведения о поставщике содержимого</span><span class="sxs-lookup"><span data-stu-id="c5109-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="c5109-132">Создание поставщика содержимого</span><span class="sxs-lookup"><span data-stu-id="c5109-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="c5109-133">Руководство разработчика Storage Access Framework</span><span class="sxs-lookup"><span data-stu-id="c5109-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

