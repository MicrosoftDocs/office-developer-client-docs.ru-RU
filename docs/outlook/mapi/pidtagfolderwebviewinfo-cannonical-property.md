---
title: Каноническое свойство PidTagFolderWebViewInfo Cannonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 62bc0e75d0a405ebe9f68ec9f4af1ca038bda219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811154"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="5f46c-103">Каноническое свойство PidTagFolderWebViewInfo Cannonical Property</span><span class="sxs-lookup"><span data-stu-id="5f46c-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="5f46c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f46c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f46c-105">Содержит URL-адрес для домашней страницы папки в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="5f46c-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="5f46c-106">Это свойство содержит двоичный поток, называется **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="5f46c-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f46c-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5f46c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f46c-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="5f46c-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="5f46c-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5f46c-109">Identifier:</span></span>  <br/> |<span data-ttu-id="5f46c-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="5f46c-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="5f46c-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5f46c-111">Data type:</span></span>  <br/> |<span data-ttu-id="5f46c-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f46c-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f46c-113">Область:</span><span class="sxs-lookup"><span data-stu-id="5f46c-113">Area:</span></span>  <br/> |<span data-ttu-id="5f46c-114">Папки MAPI</span><span class="sxs-lookup"><span data-stu-id="5f46c-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f46c-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f46c-115">Remarks</span></span>

<span data-ttu-id="5f46c-116">URL-адрес домашней страницы может использоваться для любой папки Outlook.</span><span class="sxs-lookup"><span data-stu-id="5f46c-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="5f46c-117">Эти сведения можно обратиться в Outlook из вкладка " **Домашняя страница** " диалогового окна свойств папки.</span><span class="sxs-lookup"><span data-stu-id="5f46c-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="5f46c-118">В зависимости от того, определенные параметры политики на домашнюю страницу может игнорируется с Outlook, если хранилище MAPI, содержащем эту папку не дает MSCAP_SECURE_FOLDER_HOMEPAGES в реализации [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5f46c-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="5f46c-119">Папки **Outlook сегодня** и общей папки может иметь URL-адреса домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="5f46c-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="5f46c-120">Тем не менее папки **Outlook сегодня** используется другой механизм для управления его URL-адрес домашней страницы; Этот механизм не рассматриваются в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="5f46c-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="5f46c-121">Общедоступная папка также могут иметь определенные в нем URL домашней страницы, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f46c-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="5f46c-122">Тем не менее эту возможность не описанных в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="5f46c-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="5f46c-123">Значение этого свойства — это двоичный поток, называется **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="5f46c-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="5f46c-124">Структура WebViewPersistenceObject потока</span><span class="sxs-lookup"><span data-stu-id="5f46c-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="5f46c-125">Структура потока **WebViewPersistenceObject** содержит сведения об URL-адрес домашней страницы для папки.</span><span class="sxs-lookup"><span data-stu-id="5f46c-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="5f46c-126">Элементы данных в эту структуру хранятся в прямом байтовом, сразу после друг с другом в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="5f46c-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5f46c-127">Следующее описание не список всех значений поля, поддерживаются в Outlook; Таким образом когда код считывает существующего потока, некоторые флаги, не перечисленных здесь может также найти.</span><span class="sxs-lookup"><span data-stu-id="5f46c-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="5f46c-128">Тем не менее можно использовать это описание для программного создания значения для свойства **PidTagFolderWebViewInfo** , получите представление об Outlook.</span><span class="sxs-lookup"><span data-stu-id="5f46c-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="5f46c-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="5f46c-129">_dwVersion_</span></span>
  
> <span data-ttu-id="5f46c-130">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="5f46c-130">DWORD (4 bytes).</span></span> <span data-ttu-id="5f46c-131">Версия формата структуры.</span><span class="sxs-lookup"><span data-stu-id="5f46c-131">The version of the structure's format.</span></span> <span data-ttu-id="5f46c-132">По состоянию на Microsoft Office Outlook 2007 поддерживается только значение для этого поля — следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5f46c-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="5f46c-133">**Value name**</span><span class="sxs-lookup"><span data-stu-id="5f46c-133">**Value name**</span></span>|<span data-ttu-id="5f46c-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5f46c-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f46c-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="5f46c-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="5f46c-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f46c-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="5f46c-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="5f46c-137">_dwType_</span></span>
  
> <span data-ttu-id="5f46c-138">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="5f46c-138">DWORD (4 bytes).</span></span> <span data-ttu-id="5f46c-139">Тип данных домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="5f46c-139">The type of the home page information.</span></span> <span data-ttu-id="5f46c-140">По состоянию на Microsoft Office Outlook 2007 поддерживается только значение для этого поля — следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5f46c-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="5f46c-141">**Value name**</span><span class="sxs-lookup"><span data-stu-id="5f46c-141">**Value name**</span></span>|<span data-ttu-id="5f46c-142">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5f46c-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f46c-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="5f46c-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="5f46c-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f46c-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="5f46c-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5f46c-145">_dwFlags_</span></span>
  
> <span data-ttu-id="5f46c-146">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="5f46c-146">DWORD (4 bytes).</span></span> <span data-ttu-id="5f46c-147">Сочетание ноль или больше помечает, значения и значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5f46c-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="5f46c-148">Флаг имя \*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f46c-148">****Flag name****</span></span>|<span data-ttu-id="5f46c-149">Значение \*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f46c-149">****Value****</span></span>|<span data-ttu-id="5f46c-150">****Описание****</span><span class="sxs-lookup"><span data-stu-id="5f46c-150">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f46c-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f46c-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="5f46c-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f46c-152">0x00000001</span></span>  <br/> |<span data-ttu-id="5f46c-153">На вкладке **Домашняя страница** диалоговое окно Свойства для папки установлен флажок **Показывать домашнюю страницу по умолчанию для этой папки** .</span><span class="sxs-lookup"><span data-stu-id="5f46c-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="5f46c-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="5f46c-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="5f46c-155">Массив элементов 7 DWORD (28 байт).</span><span class="sxs-lookup"><span data-stu-id="5f46c-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="5f46c-156">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5f46c-156">Unused.</span></span>
    
<span data-ttu-id="5f46c-157">cbData</span><span class="sxs-lookup"><span data-stu-id="5f46c-157">cbData</span></span>
  
> <span data-ttu-id="5f46c-158">ULONG (4 байта).</span><span class="sxs-lookup"><span data-stu-id="5f46c-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="5f46c-159">Размер в байтах, _wzURL_ элемента данных.</span><span class="sxs-lookup"><span data-stu-id="5f46c-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="5f46c-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="5f46c-160">_wzURL_</span></span>
  
> <span data-ttu-id="5f46c-161">Массив элементов WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f46c-161">An array of WCHAR elements.</span></span> <span data-ttu-id="5f46c-162">Представление UTF-16 в строке URL-адреса нулем домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="5f46c-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="5f46c-163">Пример WebViewPersistenceObject потока</span><span class="sxs-lookup"><span data-stu-id="5f46c-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="5f46c-164">В этом разделе описывается пример **WebViewPersistenceObject** потока.</span><span class="sxs-lookup"><span data-stu-id="5f46c-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="5f46c-165">Поток URL-адрес домашней страницы "http://www.microsoft.com«.</span><span class="sxs-lookup"><span data-stu-id="5f46c-165">The stream specifies the home page URL "http://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="5f46c-166">**Дамп данных**</span><span class="sxs-lookup"><span data-stu-id="5f46c-166">**Data dump**</span></span>
  
<span data-ttu-id="5f46c-167">Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="5f46c-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="5f46c-168">**Смещение потока**</span><span class="sxs-lookup"><span data-stu-id="5f46c-168">**Stream offset**</span></span>|<span data-ttu-id="5f46c-169">**Байт данных**</span><span class="sxs-lookup"><span data-stu-id="5f46c-169">**Data bytes**</span></span>|<span data-ttu-id="5f46c-170">**Данные в формате ASCII**</span><span class="sxs-lookup"><span data-stu-id="5f46c-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f46c-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="5f46c-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="5f46c-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="5f46c-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="5f46c-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="5f46c-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="5f46c-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="5f46c-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="5f46c-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="5f46c-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="5f46c-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="5f46c-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="5f46c-177">Ниже приведен синтаксического анализа образца данных для потока **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="5f46c-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="5f46c-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="5f46c-178">_dwVersion_</span></span>
  
> <span data-ttu-id="5f46c-179">Смещение 0x0, 4 байта: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="5f46c-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="5f46c-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="5f46c-180">_dwType_</span></span>
  
> <span data-ttu-id="5f46c-181">Смещение 0x4, 4 байта: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="5f46c-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="5f46c-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5f46c-182">_dwFlags_</span></span>
  
> <span data-ttu-id="5f46c-183">Смещение 0x8, 4 байта: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="5f46c-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="5f46c-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="5f46c-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="5f46c-185">Смещение 0xC 28 байтов: все нули.</span><span class="sxs-lookup"><span data-stu-id="5f46c-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="5f46c-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="5f46c-186">_cbData_</span></span>
  
> <span data-ttu-id="5f46c-187">Смещение 0x28, 4 байта: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="5f46c-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="5f46c-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="5f46c-188">_wzURL_</span></span>
  
> <span data-ttu-id="5f46c-189">Смещение 0x2C, 0x32 байт: массив 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="5f46c-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="5f46c-190">Значение нулем строку Юникод: "http://www.microsoft.com«.</span><span class="sxs-lookup"><span data-stu-id="5f46c-190">A Unicode zero-terminated string value: "http://www.microsoft.com".</span></span>
    

