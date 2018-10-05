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
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389962"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="3fcdf-103">Каноническое свойство PidTagFolderWebViewInfo Cannonical Property</span><span class="sxs-lookup"><span data-stu-id="3fcdf-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="3fcdf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fcdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fcdf-105">Содержит URL-адрес для домашней страницы папки в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="3fcdf-106">Это свойство содержит двоичный поток, называется **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fcdf-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fcdf-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="3fcdf-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="3fcdf-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-109">Identifier:</span></span>  <br/> |<span data-ttu-id="3fcdf-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="3fcdf-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="3fcdf-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-111">Data type:</span></span>  <br/> |<span data-ttu-id="3fcdf-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3fcdf-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3fcdf-113">Область:</span><span class="sxs-lookup"><span data-stu-id="3fcdf-113">Area:</span></span>  <br/> |<span data-ttu-id="3fcdf-114">Папки MAPI</span><span class="sxs-lookup"><span data-stu-id="3fcdf-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fcdf-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3fcdf-115">Remarks</span></span>

<span data-ttu-id="3fcdf-116">URL-адрес домашней страницы может использоваться для любой папки Outlook.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="3fcdf-117">Эти сведения можно обратиться в Outlook из вкладка " **Домашняя страница** " диалогового окна свойств папки.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="3fcdf-118">В зависимости от того, определенные параметры политики на домашнюю страницу может игнорируется с Outlook, если хранилище MAPI, содержащем эту папку не дает MSCAP_SECURE_FOLDER_HOMEPAGES в реализации [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3fcdf-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="3fcdf-119">Папки **Outlook сегодня** и общей папки может иметь URL-адреса домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="3fcdf-120">Тем не менее папки **Outlook сегодня** используется другой механизм для управления его URL-адрес домашней страницы; Этот механизм не рассматриваются в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="3fcdf-121">Общедоступная папка также могут иметь определенные в нем URL домашней страницы, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="3fcdf-122">Тем не менее эту возможность не описанных в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="3fcdf-123">Значение этого свойства — это двоичный поток, называется **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="3fcdf-124">Структура WebViewPersistenceObject потока</span><span class="sxs-lookup"><span data-stu-id="3fcdf-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="3fcdf-125">Структура потока **WebViewPersistenceObject** содержит сведения об URL-адрес домашней страницы для папки.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="3fcdf-126">Элементы данных в эту структуру хранятся в прямом байтовом, сразу после друг с другом в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3fcdf-127">Следующее описание не список всех значений поля, поддерживаются в Outlook; Таким образом когда код считывает существующего потока, некоторые флаги, не перечисленных здесь может также найти.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="3fcdf-128">Тем не менее можно использовать это описание для программного создания значения для свойства **PidTagFolderWebViewInfo** , получите представление об Outlook.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="3fcdf-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-129">_dwVersion_</span></span>
  
> <span data-ttu-id="3fcdf-130">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-130">DWORD (4 bytes).</span></span> <span data-ttu-id="3fcdf-131">Версия формата структуры.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-131">The version of the structure's format.</span></span> <span data-ttu-id="3fcdf-132">По состоянию на Microsoft Office Outlook 2007 поддерживается только значение для этого поля — следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="3fcdf-133">**Value name**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-133">**Value name**</span></span>|<span data-ttu-id="3fcdf-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3fcdf-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="3fcdf-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="3fcdf-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3fcdf-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="3fcdf-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-137">_dwType_</span></span>
  
> <span data-ttu-id="3fcdf-138">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-138">DWORD (4 bytes).</span></span> <span data-ttu-id="3fcdf-139">Тип данных домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-139">The type of the home page information.</span></span> <span data-ttu-id="3fcdf-140">По состоянию на Microsoft Office Outlook 2007 поддерживается только значение для этого поля — следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="3fcdf-141">**Value name**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-141">**Value name**</span></span>|<span data-ttu-id="3fcdf-142">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3fcdf-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="3fcdf-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="3fcdf-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3fcdf-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="3fcdf-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-145">_dwFlags_</span></span>
  
> <span data-ttu-id="3fcdf-146">Значение DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-146">DWORD (4 bytes).</span></span> <span data-ttu-id="3fcdf-147">Сочетание ноль или больше помечает, значения и значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="3fcdf-148">Флаг имя \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3fcdf-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="3fcdf-149">Значение \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3fcdf-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="3fcdf-150">\*\*\*\*Описание\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3fcdf-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3fcdf-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3fcdf-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="3fcdf-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3fcdf-152">0x00000001</span></span>  <br/> |<span data-ttu-id="3fcdf-153">На вкладке **Домашняя страница** диалоговое окно Свойства для папки установлен флажок **Показывать домашнюю страницу по умолчанию для этой папки** .</span><span class="sxs-lookup"><span data-stu-id="3fcdf-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="3fcdf-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="3fcdf-155">Массив элементов 7 DWORD (28 байт).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="3fcdf-156">Не используется.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-156">Unused.</span></span>
    
<span data-ttu-id="3fcdf-157">cbData</span><span class="sxs-lookup"><span data-stu-id="3fcdf-157">cbData</span></span>
  
> <span data-ttu-id="3fcdf-158">ULONG (4 байта).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="3fcdf-159">Размер в байтах, _wzURL_ элемента данных.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="3fcdf-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-160">_wzURL_</span></span>
  
> <span data-ttu-id="3fcdf-161">Массив элементов WCHAR.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-161">An array of WCHAR elements.</span></span> <span data-ttu-id="3fcdf-162">Представление UTF-16 в строке URL-адреса нулем домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="3fcdf-163">Пример WebViewPersistenceObject потока</span><span class="sxs-lookup"><span data-stu-id="3fcdf-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="3fcdf-164">В этом разделе описывается пример **WebViewPersistenceObject** потока.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="3fcdf-165">Поток URL-адрес домашней страницы "https://www.microsoft.com«.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="3fcdf-166">**Дамп данных**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-166">**Data dump**</span></span>
  
<span data-ttu-id="3fcdf-167">Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="3fcdf-168">**Смещение потока**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-168">**Stream offset**</span></span>|<span data-ttu-id="3fcdf-169">**Байт данных**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-169">**Data bytes**</span></span>|<span data-ttu-id="3fcdf-170">**Данные в формате ASCII**</span><span class="sxs-lookup"><span data-stu-id="3fcdf-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3fcdf-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="3fcdf-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="3fcdf-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="3fcdf-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="3fcdf-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="3fcdf-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="3fcdf-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="3fcdf-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="3fcdf-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="3fcdf-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="3fcdf-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="3fcdf-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="3fcdf-177">Ниже приведен синтаксического анализа образца данных для потока **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="3fcdf-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="3fcdf-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-178">_dwVersion_</span></span>
  
> <span data-ttu-id="3fcdf-179">Смещение 0x0, 4 байта: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="3fcdf-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-180">_dwType_</span></span>
  
> <span data-ttu-id="3fcdf-181">Смещение 0x4, 4 байта: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="3fcdf-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-182">_dwFlags_</span></span>
  
> <span data-ttu-id="3fcdf-183">Смещение 0x8, 4 байта: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="3fcdf-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="3fcdf-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="3fcdf-185">Смещение 0xC 28 байтов: все нули.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="3fcdf-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-186">_cbData_</span></span>
  
> <span data-ttu-id="3fcdf-187">Смещение 0x28, 4 байта: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="3fcdf-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="3fcdf-188">_wzURL_</span></span>
  
> <span data-ttu-id="3fcdf-189">Смещение 0x2C, 0x32 байт: массив 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="3fcdf-190">Значение нулем строку Юникод: "https://www.microsoft.com«.</span><span class="sxs-lookup"><span data-stu-id="3fcdf-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

