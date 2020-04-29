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
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="e4f85-103">Каноническое свойство PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="e4f85-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="e4f85-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4f85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4f85-105">Содержит URL-адрес домашней страницы папки в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="e4f85-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="e4f85-106">Это свойство содержит двоичный поток с именем **вебвиевперсистенцеобжект**.</span><span class="sxs-lookup"><span data-stu-id="e4f85-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4f85-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e4f85-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4f85-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="e4f85-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="e4f85-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e4f85-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e4f85-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="e4f85-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="e4f85-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e4f85-111">Data type:</span></span>  <br/> |<span data-ttu-id="e4f85-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e4f85-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e4f85-113">Область:</span><span class="sxs-lookup"><span data-stu-id="e4f85-113">Area:</span></span>  <br/> |<span data-ttu-id="e4f85-114">Папка MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f85-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4f85-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4f85-115">Remarks</span></span>

<span data-ttu-id="e4f85-116">URL-адрес домашней страницы можно указать для любой папки Outlook.</span><span class="sxs-lookup"><span data-stu-id="e4f85-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="e4f85-117">Эту информацию можно получить в Outlook на вкладке " **Домашняя страница** " диалогового окна Свойства для папки.</span><span class="sxs-lookup"><span data-stu-id="e4f85-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="e4f85-118">В зависимости от определенных параметров политики Домашняя страница может быть проигнорирована в Outlook, если хранилище MAPI, содержащее эту папку, не сообщает о MSCAP_SECURE_FOLDER_HOMEPAGES в своей реализации [IMSCapabilities:: Capabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f85-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="e4f85-119">В папке " **Outlook сегодня** " и в общедоступной папке могут быть URL-адреса домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="e4f85-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="e4f85-120">Однако папка " **Outlook сегодня** " использует другой механизм для управления URL-адресом домашней страницы; Этот механизм не рассматривается в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e4f85-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="e4f85-121">В общедоступной папке также может быть определен URL-адрес домашней страницы, относящийся к конкретному пользователю.</span><span class="sxs-lookup"><span data-stu-id="e4f85-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="e4f85-122">Однако эта возможность не описывается в этой статье.</span><span class="sxs-lookup"><span data-stu-id="e4f85-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="e4f85-123">Значение этого свойства является двоичным потоком, который называется **вебвиевперсистенцеобжект**.</span><span class="sxs-lookup"><span data-stu-id="e4f85-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="e4f85-124">Структура потока Вебвиевперсистенцеобжект</span><span class="sxs-lookup"><span data-stu-id="e4f85-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="e4f85-125">Структура потока **вебвиевперсистенцеобжект** содержит сведения об URL-адресе домашней страницы для папки.</span><span class="sxs-lookup"><span data-stu-id="e4f85-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="e4f85-126">Элементы данных в этой структуре хранятся в обратном байтовом порядке, непосредственно следующем за другим в приведенном ниже указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="e4f85-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e4f85-127">Следующее описание может не перечислить все значения полей, поддерживаемые в Outlook; Таким образом, когда код читает существующий поток, некоторые флаги, которые не указаны здесь, также могут быть найдены.</span><span class="sxs-lookup"><span data-stu-id="e4f85-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="e4f85-128">Однако это описание можно использовать для программного создания значений для свойства **каноническое pidtagfolderwebviewinfo** , которое будет понято в Outlook.</span><span class="sxs-lookup"><span data-stu-id="e4f85-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="e4f85-129">_двверсион_</span><span class="sxs-lookup"><span data-stu-id="e4f85-129">_dwVersion_</span></span>
  
> <span data-ttu-id="e4f85-130">DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="e4f85-130">DWORD (4 bytes).</span></span> <span data-ttu-id="e4f85-131">Версия формата структуры.</span><span class="sxs-lookup"><span data-stu-id="e4f85-131">The version of the structure's format.</span></span> <span data-ttu-id="e4f85-132">По мере использования Microsoft Office Outlook 2007 для этого поля поддерживается только следующее значение.</span><span class="sxs-lookup"><span data-stu-id="e4f85-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="e4f85-133">**Имя значения**</span><span class="sxs-lookup"><span data-stu-id="e4f85-133">**Value name**</span></span>|<span data-ttu-id="e4f85-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e4f85-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4f85-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="e4f85-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="e4f85-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e4f85-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="e4f85-137">_двтипе_</span><span class="sxs-lookup"><span data-stu-id="e4f85-137">_dwType_</span></span>
  
> <span data-ttu-id="e4f85-138">DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="e4f85-138">DWORD (4 bytes).</span></span> <span data-ttu-id="e4f85-139">Тип данных домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="e4f85-139">The type of the home page information.</span></span> <span data-ttu-id="e4f85-140">По мере использования Microsoft Office Outlook 2007 для этого поля поддерживается только следующее значение.</span><span class="sxs-lookup"><span data-stu-id="e4f85-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="e4f85-141">**Имя значения**</span><span class="sxs-lookup"><span data-stu-id="e4f85-141">**Value name**</span></span>|<span data-ttu-id="e4f85-142">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e4f85-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4f85-143">вебвиевурл</span><span class="sxs-lookup"><span data-stu-id="e4f85-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="e4f85-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4f85-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="e4f85-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e4f85-145">_dwFlags_</span></span>
  
> <span data-ttu-id="e4f85-146">DWORD (4 байта).</span><span class="sxs-lookup"><span data-stu-id="e4f85-146">DWORD (4 bytes).</span></span> <span data-ttu-id="e4f85-147">Сочетание нулевого или большего числа флагов, значения и значения которых перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e4f85-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="e4f85-148">Имя флага \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="e4f85-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="e4f85-149">\*\*\*\*Value\*\* (Значение)\*\*</span><span class="sxs-lookup"><span data-stu-id="e4f85-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="e4f85-150">\*\*\*\*Описание\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e4f85-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4f85-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="e4f85-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="e4f85-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4f85-152">0x00000001</span></span>  <br/> |<span data-ttu-id="e4f85-153">Флажок **Показывать домашнюю страницу по умолчанию для этой папки** установлен на вкладке " **Домашняя страница** " диалогового окна Свойства для папки.</span><span class="sxs-lookup"><span data-stu-id="e4f85-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="e4f85-154">_Двунусед [7]_</span><span class="sxs-lookup"><span data-stu-id="e4f85-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="e4f85-155">Массив из 7 элементов DWORD (всего 28 байт).</span><span class="sxs-lookup"><span data-stu-id="e4f85-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="e4f85-156">Неиспользуемых.</span><span class="sxs-lookup"><span data-stu-id="e4f85-156">Unused.</span></span>
    
<span data-ttu-id="e4f85-157">кбдата</span><span class="sxs-lookup"><span data-stu-id="e4f85-157">cbData</span></span>
  
> <span data-ttu-id="e4f85-158">ULONG (4 байта).</span><span class="sxs-lookup"><span data-stu-id="e4f85-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="e4f85-159">Размер элемента данных _взурл_ в байтах.</span><span class="sxs-lookup"><span data-stu-id="e4f85-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="e4f85-160">_взурл_</span><span class="sxs-lookup"><span data-stu-id="e4f85-160">_wzURL_</span></span>
  
> <span data-ttu-id="e4f85-161">Массив элементов типа WCHAR.</span><span class="sxs-lookup"><span data-stu-id="e4f85-161">An array of WCHAR elements.</span></span> <span data-ttu-id="e4f85-162">Представление UTF-16 строки URL-адреса домашней страницы, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="e4f85-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="e4f85-163">Пример потока Вебвиевперсистенцеобжект</span><span class="sxs-lookup"><span data-stu-id="e4f85-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="e4f85-164">В этом разделе описывается пример потока **вебвиевперсистенцеобжект** .</span><span class="sxs-lookup"><span data-stu-id="e4f85-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="e4f85-165">В этом потоке указывается URL-адресhttps://www.microsoft.comдомашней страницы "".</span><span class="sxs-lookup"><span data-stu-id="e4f85-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="e4f85-166">**Дамп данных**</span><span class="sxs-lookup"><span data-stu-id="e4f85-166">**Data dump**</span></span>
  
<span data-ttu-id="e4f85-167">Ниже приведен дамп данных потока, как он будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="e4f85-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="e4f85-168">**Смещение потока**</span><span class="sxs-lookup"><span data-stu-id="e4f85-168">**Stream offset**</span></span>|<span data-ttu-id="e4f85-169">**Байты данных**</span><span class="sxs-lookup"><span data-stu-id="e4f85-169">**Data bytes**</span></span>|<span data-ttu-id="e4f85-170">**Данные ASCII**</span><span class="sxs-lookup"><span data-stu-id="e4f85-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4f85-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="e4f85-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="e4f85-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="e4f85-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="e4f85-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="e4f85-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="e4f85-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="e4f85-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="e4f85-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="e4f85-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="e4f85-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="e4f85-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="e4f85-177">Ниже приведен пример синтаксического анализа данных для потока **вебвиевперсистенцеобжект** .</span><span class="sxs-lookup"><span data-stu-id="e4f85-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="e4f85-178">_двверсион_</span><span class="sxs-lookup"><span data-stu-id="e4f85-178">_dwVersion_</span></span>
  
> <span data-ttu-id="e4f85-179">Смещение 0x0, 4 байта: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="e4f85-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="e4f85-180">_двтипе_</span><span class="sxs-lookup"><span data-stu-id="e4f85-180">_dwType_</span></span>
  
> <span data-ttu-id="e4f85-181">Смещение 0x4, 4 байта: 0x00000001 (ВЕБВИЕВУРЛ).</span><span class="sxs-lookup"><span data-stu-id="e4f85-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="e4f85-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e4f85-182">_dwFlags_</span></span>
  
> <span data-ttu-id="e4f85-183">Смещение 0x8, 4 байта: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="e4f85-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="e4f85-184">_Двунусед [7]_</span><span class="sxs-lookup"><span data-stu-id="e4f85-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="e4f85-185">Смещение 0xC, 28 байтов: все нули.</span><span class="sxs-lookup"><span data-stu-id="e4f85-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="e4f85-186">_кбдата_</span><span class="sxs-lookup"><span data-stu-id="e4f85-186">_cbData_</span></span>
  
> <span data-ttu-id="e4f85-187">Офсетная 0x28, 4 байта: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="e4f85-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="e4f85-188">_взурл_</span><span class="sxs-lookup"><span data-stu-id="e4f85-188">_wzURL_</span></span>
  
> <span data-ttu-id="e4f85-189">Смещение 0x2C, 0x32 байт: массив из 25 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="e4f85-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="e4f85-190">Строковое значение Юникода с нулевым нулем: "https://www.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="e4f85-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

