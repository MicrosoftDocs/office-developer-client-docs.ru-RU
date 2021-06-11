---
title: Каноническое свойство PidTagFolderWebViewInfo
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316312"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="ef275-103">Каноническое свойство PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="ef275-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="ef275-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef275-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef275-105">Содержит URL-адрес домашней страницы папки в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="ef275-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="ef275-106">Это свойство содержит двоичный поток под названием **WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="ef275-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef275-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef275-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef275-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="ef275-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="ef275-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef275-109">Identifier:</span></span>  <br/> |<span data-ttu-id="ef275-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="ef275-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="ef275-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef275-111">Data type:</span></span>  <br/> |<span data-ttu-id="ef275-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ef275-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ef275-113">Область:</span><span class="sxs-lookup"><span data-stu-id="ef275-113">Area:</span></span>  <br/> |<span data-ttu-id="ef275-114">Папка MAPI</span><span class="sxs-lookup"><span data-stu-id="ef275-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef275-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef275-115">Remarks</span></span>

<span data-ttu-id="ef275-116">URL-адрес домашней страницы может быть указан для любой Outlook папки.</span><span class="sxs-lookup"><span data-stu-id="ef275-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="ef275-117">Эти сведения можно получить в Outlook на вкладке **Главная** страница диалогового окна Свойства для папки.</span><span class="sxs-lookup"><span data-stu-id="ef275-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="ef275-118">В зависимости от определенных параметров политики главная страница может быть проигнорирована Outlook если магазин MAPI, содержащий эту папку, не сообщает MSCAP_SECURE_FOLDER_HOMEPAGES в реализации [IMSCapabilities::GetCapabilities.](pidtagfolderwebviewinfo-cannonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ef275-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="ef275-119">И **папка Outlook Today,** и общедоступные папки могут иметь URL-адреса домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="ef275-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="ef275-120">Однако **папка Outlook Today** использует другой механизм для управления URL-адресом домашней страницы; этот механизм не охватывается в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ef275-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="ef275-121">В общедоступных папках также может быть определен URL-адрес домашней страницы, который является специфическим для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef275-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="ef275-122">Однако эта возможность не описана в этой теме.</span><span class="sxs-lookup"><span data-stu-id="ef275-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="ef275-123">Значение этого свойства — двоичный поток, называемый **WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="ef275-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="ef275-124">Структура потока WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="ef275-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="ef275-125">Структура **потока WebViewPersistenceObject** содержит сведения о URL-адресе домашней страницы для папки.</span><span class="sxs-lookup"><span data-stu-id="ef275-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="ef275-126">Элементы данных в этой структуре хранятся в порядке маленького byte, сразу же следуя друг за другом в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="ef275-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ef275-127">В следующем описании не может быть списка всех значений поля, поддерживаемых Outlook; Поэтому при считываемом кодом существующем потоке также могут быть найдены некоторые флаги, которые здесь не указаны.</span><span class="sxs-lookup"><span data-stu-id="ef275-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="ef275-128">Однако это описание можно использовать для программного создания значений для свойства **PidTagFolderWebViewInfo,** которое Outlook понять.</span><span class="sxs-lookup"><span data-stu-id="ef275-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="ef275-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="ef275-129">_dwVersion_</span></span>
  
> <span data-ttu-id="ef275-130">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="ef275-130">DWORD (4 bytes).</span></span> <span data-ttu-id="ef275-131">Версия формата структуры.</span><span class="sxs-lookup"><span data-stu-id="ef275-131">The version of the structure's format.</span></span> <span data-ttu-id="ef275-132">По Microsoft Office Outlook 2007 г. для этого поля поддерживается только одно значение.</span><span class="sxs-lookup"><span data-stu-id="ef275-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="ef275-133">**Имя значения**</span><span class="sxs-lookup"><span data-stu-id="ef275-133">**Value name**</span></span>|<span data-ttu-id="ef275-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ef275-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef275-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="ef275-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="ef275-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ef275-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="ef275-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="ef275-137">_dwType_</span></span>
  
> <span data-ttu-id="ef275-138">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="ef275-138">DWORD (4 bytes).</span></span> <span data-ttu-id="ef275-139">Тип сведений о домашней странице.</span><span class="sxs-lookup"><span data-stu-id="ef275-139">The type of the home page information.</span></span> <span data-ttu-id="ef275-140">По Microsoft Office Outlook 2007 г. для этого поля поддерживается только одно значение.</span><span class="sxs-lookup"><span data-stu-id="ef275-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="ef275-141">**Имя значения**</span><span class="sxs-lookup"><span data-stu-id="ef275-141">**Value name**</span></span>|<span data-ttu-id="ef275-142">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ef275-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef275-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="ef275-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="ef275-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ef275-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="ef275-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="ef275-145">_dwFlags_</span></span>
  
> <span data-ttu-id="ef275-146">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="ef275-146">DWORD (4 bytes).</span></span> <span data-ttu-id="ef275-147">Сочетание нулей или нескольких флагов, значения и значения которых перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ef275-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="ef275-148">Имя флага\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ef275-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="ef275-149">\*\*\*\*Value\*\* (Значение)\*\*</span><span class="sxs-lookup"><span data-stu-id="ef275-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="ef275-150">\*\*\*\*Описание\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ef275-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef275-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef275-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="ef275-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ef275-152">0x00000001</span></span>  <br/> |<span data-ttu-id="ef275-153">Главная **страница Show по** умолчанию для этого папки  была проверена на вкладке Главная страница диалоговое окно Свойства для папки.</span><span class="sxs-lookup"><span data-stu-id="ef275-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="ef275-154">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="ef275-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="ef275-155">Массив из 7 элементов DWORD (всего 28 bytes).</span><span class="sxs-lookup"><span data-stu-id="ef275-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="ef275-156">Неиспользовано.</span><span class="sxs-lookup"><span data-stu-id="ef275-156">Unused.</span></span>
    
<span data-ttu-id="ef275-157">cbData</span><span class="sxs-lookup"><span data-stu-id="ef275-157">cbData</span></span>
  
> <span data-ttu-id="ef275-158">ULONG (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="ef275-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="ef275-159">Размер элемента  _данных wzURL_ в байтах.</span><span class="sxs-lookup"><span data-stu-id="ef275-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="ef275-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="ef275-160">_wzURL_</span></span>
  
> <span data-ttu-id="ef275-161">Массив элементов WCHAR.</span><span class="sxs-lookup"><span data-stu-id="ef275-161">An array of WCHAR elements.</span></span> <span data-ttu-id="ef275-162">Представление UTF-16 строки URL-адреса домашней страницы с нулевым прекращением.</span><span class="sxs-lookup"><span data-stu-id="ef275-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="ef275-163">Образец потока WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="ef275-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="ef275-164">В этом разделе описывается пример потока **WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="ef275-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="ef275-165">Поток указывает URL-адрес домашней страницы " https://www.microsoft.com ".</span><span class="sxs-lookup"><span data-stu-id="ef275-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="ef275-166">**Сброс данных**</span><span class="sxs-lookup"><span data-stu-id="ef275-166">**Data dump**</span></span>
  
<span data-ttu-id="ef275-167">Ниже приводится сброс данных потока, который будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="ef275-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="ef275-168">**Смещение потока**</span><span class="sxs-lookup"><span data-stu-id="ef275-168">**Stream offset**</span></span>|<span data-ttu-id="ef275-169">**Bytes data**</span><span class="sxs-lookup"><span data-stu-id="ef275-169">**Data bytes**</span></span>|<span data-ttu-id="ef275-170">**Данные ASCII**</span><span class="sxs-lookup"><span data-stu-id="ef275-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef275-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="ef275-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="ef275-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="ef275-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="ef275-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="ef275-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="ef275-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="ef275-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="ef275-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="ef275-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="ef275-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="ef275-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="ef275-177">Ниже приводится анализ примерных данных для **потока WebViewPersistenceObject.**</span><span class="sxs-lookup"><span data-stu-id="ef275-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="ef275-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="ef275-178">_dwVersion_</span></span>
  
> <span data-ttu-id="ef275-179">Смещение 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="ef275-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="ef275-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="ef275-180">_dwType_</span></span>
  
> <span data-ttu-id="ef275-181">Смещение 0x4, 4 байта: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="ef275-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="ef275-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="ef275-182">_dwFlags_</span></span>
  
> <span data-ttu-id="ef275-183">Смещение 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="ef275-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="ef275-184">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="ef275-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="ef275-185">Смещение 0xC, 28 bytes: все нули.</span><span class="sxs-lookup"><span data-stu-id="ef275-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="ef275-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="ef275-186">_cbData_</span></span>
  
> <span data-ttu-id="ef275-187">Смещение 0x28, 4 bytes: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="ef275-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="ef275-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="ef275-188">_wzURL_</span></span>
  
> <span data-ttu-id="ef275-189">Смещение 0x2C, 0x32 байтов: массив из 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ef275-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="ef275-190">Значение строки с нулевой строкой Unicode: https://www.microsoft.com ".</span><span class="sxs-lookup"><span data-stu-id="ef275-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

