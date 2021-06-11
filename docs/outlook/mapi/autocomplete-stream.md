---
title: Поток автозаполнения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aadfba3e2674c35019a2e5f3eb374fbed1ad2a75
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734226"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="562cb-103">Поток автозаполнения</span><span class="sxs-lookup"><span data-stu-id="562cb-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="562cb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="562cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="562cb-105">Необходимо понимать не только то, как Microsoft Outlook взаимодействует с потоком автозаполнения, но и двоичный формат потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="562cb-106">Поток автозаполнения — это набор строк свойств получателя, который сохраняется в виде двоичного потока вместе с некоторыми метаданными, которые используются только Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 и Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="562cb-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="562cb-107">Метаданные относятся к взаимодействиям Outlook с потоком автозаполнения, поэтому третьим сторонам необходимо сохранять содержимое каждого блока метаданных при сохранении измененного потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="562cb-108">Иными словами, третьим сторонам следует изменить только часть с набором строк двоичного формата и сохранить изначальное содержимое блока метаданных для потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="562cb-109">Визуализация потока</span><span class="sxs-lookup"><span data-stu-id="562cb-109">Stream Visualization</span></span>

<span data-ttu-id="562cb-110">Высокоуровневая структура потока автозаполнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="562cb-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="562cb-111">метаданные (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="562cb-112">основной номер версии (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="562cb-113">дополнительный номер версии (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="562cb-114">количество строк n (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="562cb-115">количество свойств p в первой строке (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="562cb-116">тег свойства 1 (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="562cb-117">зарезервированные данные свойства 1 (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="562cb-118">объединение значений для свойства 1 (8 байтов);</span><span class="sxs-lookup"><span data-stu-id="562cb-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="562cb-119">данные значения свойства 1 (байты переменной или 0);</span><span class="sxs-lookup"><span data-stu-id="562cb-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="562cb-120">…</span><span class="sxs-lookup"><span data-stu-id="562cb-120">…</span></span> <span data-ttu-id="562cb-121">свойства (от свойства 2 до свойства P-1);</span><span class="sxs-lookup"><span data-stu-id="562cb-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="562cb-122">тег свойства p (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="562cb-123">зарезервированные данные свойства p (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="562cb-124">объединение значений для свойства p (8 байтов);</span><span class="sxs-lookup"><span data-stu-id="562cb-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="562cb-125">данные значения свойства p (байты переменной или 0);</span><span class="sxs-lookup"><span data-stu-id="562cb-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="562cb-126">количество свойств q в строке второй (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="562cb-127">…</span><span class="sxs-lookup"><span data-stu-id="562cb-127">…</span></span> <span data-ttu-id="562cb-128">свойства строки второй;</span><span class="sxs-lookup"><span data-stu-id="562cb-128">(row two's properties)</span></span>
  
<span data-ttu-id="562cb-129">…</span><span class="sxs-lookup"><span data-stu-id="562cb-129">…</span></span> <span data-ttu-id="562cb-130">строки (от строки 3 до строки n-1);</span><span class="sxs-lookup"><span data-stu-id="562cb-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="562cb-131">количество свойств r в строке n (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="562cb-132">…</span><span class="sxs-lookup"><span data-stu-id="562cb-132">…</span></span> <span data-ttu-id="562cb-133">свойства строки n;</span><span class="sxs-lookup"><span data-stu-id="562cb-133">(row n's properties)</span></span>
  
<span data-ttu-id="562cb-134">количество байтов дополнительных сведений EI (4 байта);</span><span class="sxs-lookup"><span data-stu-id="562cb-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="562cb-135">дополнительные сведения (байты EI);</span><span class="sxs-lookup"><span data-stu-id="562cb-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="562cb-136">метаданные (8 байтов).</span><span class="sxs-lookup"><span data-stu-id="562cb-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="562cb-137">Пример двоичной структуры см. в разделе "Binary Example" (Пример двоичной структуры) документа [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf) (Рекомендации разработчикам и сведения о формате NK2 файлов Outlook 2003/2007).</span><span class="sxs-lookup"><span data-stu-id="562cb-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="562cb-138">Высокоуровневая структура</span><span class="sxs-lookup"><span data-stu-id="562cb-138">High-level Layout</span></span>

<span data-ttu-id="562cb-139">В целом структура потока автозаполнения выглядит указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="562cb-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="562cb-140">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-140">**Value Data**</span></span>|<span data-ttu-id="562cb-141">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-142">Метаданные</span><span class="sxs-lookup"><span data-stu-id="562cb-142">Metadata</span></span>  <br/> |<span data-ttu-id="562cb-143">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-143">4</span></span>  <br/> |
|<span data-ttu-id="562cb-144">Основной номер версии</span><span class="sxs-lookup"><span data-stu-id="562cb-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="562cb-145">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-145">4</span></span>  <br/> |
|<span data-ttu-id="562cb-146">Дополнительный номер версии</span><span class="sxs-lookup"><span data-stu-id="562cb-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="562cb-147">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-147">4</span></span>  <br/> |
|<span data-ttu-id="562cb-148">Набор строк</span><span class="sxs-lookup"><span data-stu-id="562cb-148">Row-set</span></span>  <br/> |<span data-ttu-id="562cb-149">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-149">Variable</span></span>  <br/> |
|<span data-ttu-id="562cb-150">Количество байтов дополнительных сведений EI</span><span class="sxs-lookup"><span data-stu-id="562cb-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="562cb-151">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-151">4</span></span>  <br/> |
|<span data-ttu-id="562cb-152">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="562cb-152">Extra information</span></span>  <br/> |<span data-ttu-id="562cb-153">EI</span><span class="sxs-lookup"><span data-stu-id="562cb-153">EI</span></span>  <br/> |
|<span data-ttu-id="562cb-154">Метаданные</span><span class="sxs-lookup"><span data-stu-id="562cb-154">Metadata</span></span>  <br/> |<span data-ttu-id="562cb-155">8 </span><span class="sxs-lookup"><span data-stu-id="562cb-155">8</span></span>  <br/> |
   
<span data-ttu-id="562cb-156">Если при чтении потока обнаружено, что основной номер версии отличается от 12, то этот поток не следует читать или же записывать.</span><span class="sxs-lookup"><span data-stu-id="562cb-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="562cb-157">Текущий дополнительный номер версии потока автозаполнения — 0, то есть количество байтов дополнительной информации равно 0.</span><span class="sxs-lookup"><span data-stu-id="562cb-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="562cb-158">Если дополнительный номер версии отличается от 0, то будет присутствовать дополнительная информация, которую необходимо прочесть во время чтения потока и сохранить при записывании потока.</span><span class="sxs-lookup"><span data-stu-id="562cb-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="562cb-159">Кроме того, при записывании потока необходимо будет сохранить дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="562cb-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="562cb-160">Если не сохранить ни одно из этих значений, данные в записавших дополнительную информацию экземплярах Outlook будут утеряны.</span><span class="sxs-lookup"><span data-stu-id="562cb-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="562cb-161">Приложения не должны добавлять пользовательские данные в поле дополнительной информации и менять дополнительный номер версии, так как эта функциональность предназначена для поддержки расширений формата для Outlook, а не произвольных сторонних расширений.</span><span class="sxs-lookup"><span data-stu-id="562cb-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="562cb-162">Структура набора строк</span><span class="sxs-lookup"><span data-stu-id="562cb-162">Row-set Layout</span></span>

<span data-ttu-id="562cb-163">Структура набора строк выглядит указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="562cb-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="562cb-164">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-164">**Value Data**</span></span>|<span data-ttu-id="562cb-165">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-166">Количество строк</span><span class="sxs-lookup"><span data-stu-id="562cb-166">Number of rows</span></span>  <br/> |<span data-ttu-id="562cb-167">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-167">4</span></span>  <br/> |
|<span data-ttu-id="562cb-168">Строки</span><span class="sxs-lookup"><span data-stu-id="562cb-168">Rows</span></span>  <br/> |<span data-ttu-id="562cb-169">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="562cb-170">Количество строк определяет, сколько строк попадает в следующую часть последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="562cb-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="562cb-171">Структура строки</span><span class="sxs-lookup"><span data-stu-id="562cb-171">Row Layout</span></span>

<span data-ttu-id="562cb-172">Каждая строка имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="562cb-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="562cb-173">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-173">**Value Data**</span></span>|<span data-ttu-id="562cb-174">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-175">Количество свойств</span><span class="sxs-lookup"><span data-stu-id="562cb-175">Number of properties</span></span>  <br/> |<span data-ttu-id="562cb-176">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-176">4</span></span>  <br/> |
|<span data-ttu-id="562cb-177">Свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-177">Properties</span></span>  <br/> |<span data-ttu-id="562cb-178">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="562cb-179">Количество свойств определяет, сколько свойств попадает в следующую часть последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="562cb-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="562cb-180">Структура свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-180">Property Layout</span></span>

<span data-ttu-id="562cb-181">Каждое свойство имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="562cb-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="562cb-182">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-182">**Value Data**</span></span>|<span data-ttu-id="562cb-183">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-184">Тег свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-184">Property Tag</span></span>  <br/> |<span data-ttu-id="562cb-185">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-185">4</span></span>  <br/> |
|<span data-ttu-id="562cb-186">Зарезервированные данные</span><span class="sxs-lookup"><span data-stu-id="562cb-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="562cb-187">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-187">4</span></span>  <br/> |
|<span data-ttu-id="562cb-188">Объединение значений свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="562cb-189">Данные значения</span><span class="sxs-lookup"><span data-stu-id="562cb-189">Value Data</span></span>  <br/> |<span data-ttu-id="562cb-190">0 или переменная (в зависимости от тега свойства)</span><span class="sxs-lookup"><span data-stu-id="562cb-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="562cb-191">Интерпретация значения свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-191">Interpreting the Property Value</span></span>

<span data-ttu-id="562cb-192">Объединение значений свойства и данные значения следует интерпретировать с учетом тега свойства в первых 4 байтах блока свойства.</span><span class="sxs-lookup"><span data-stu-id="562cb-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="562cb-193">У этого тега свойства такой же формат, как и у тега свойства в MAPI.</span><span class="sxs-lookup"><span data-stu-id="562cb-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="562cb-194">Биты от 0 до 15 тега свойства соответствуют типу свойства.</span><span class="sxs-lookup"><span data-stu-id="562cb-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="562cb-195">Биты от 16 до 31 соответствуют идентификатору свойства.</span><span class="sxs-lookup"><span data-stu-id="562cb-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="562cb-196">Тип свойства определяет, как следует читать остальные данные свойства.</span><span class="sxs-lookup"><span data-stu-id="562cb-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="562cb-197">Статическое значение</span><span class="sxs-lookup"><span data-stu-id="562cb-197">Static Value</span></span>

<span data-ttu-id="562cb-198">Некоторые свойства не имеют данных значения, у них есть только данные объединения.</span><span class="sxs-lookup"><span data-stu-id="562cb-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="562cb-199">Ниже показано, как для типов свойств, которые следуют из тега свойства, должны интерпретироваться 8-байтовые данные объединения свойств.</span><span class="sxs-lookup"><span data-stu-id="562cb-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="562cb-200">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="562cb-200">**Prop Type**</span></span>|<span data-ttu-id="562cb-201">**Интерпретация объединения свойств**</span><span class="sxs-lookup"><span data-stu-id="562cb-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="562cb-202">PT_I2</span></span>  <br/> |<span data-ttu-id="562cb-203">short int</span><span class="sxs-lookup"><span data-stu-id="562cb-203">short int</span></span>  <br/> |
|<span data-ttu-id="562cb-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="562cb-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="562cb-205">long</span><span class="sxs-lookup"><span data-stu-id="562cb-205">long</span></span>  <br/> |
|<span data-ttu-id="562cb-206">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="562cb-206">PT_ERROR</span></span>  <br/> |<span data-ttu-id="562cb-207">long</span><span class="sxs-lookup"><span data-stu-id="562cb-207">long</span></span>  <br/> |
|<span data-ttu-id="562cb-208">PT_R4</span><span class="sxs-lookup"><span data-stu-id="562cb-208">PT_R4</span></span>  <br/> |<span data-ttu-id="562cb-209">float</span><span class="sxs-lookup"><span data-stu-id="562cb-209">float</span></span>  <br/> |
|<span data-ttu-id="562cb-210">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="562cb-210">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="562cb-211">double</span><span class="sxs-lookup"><span data-stu-id="562cb-211">double</span></span>  <br/> |
|<span data-ttu-id="562cb-212">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="562cb-212">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="562cb-213">short int</span><span class="sxs-lookup"><span data-stu-id="562cb-213">short int</span></span>  <br/> |
|<span data-ttu-id="562cb-214">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="562cb-214">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="562cb-215">FILETIME</span><span class="sxs-lookup"><span data-stu-id="562cb-215">FILETIME</span></span>  <br/> |
|<span data-ttu-id="562cb-216">PT_I8</span><span class="sxs-lookup"><span data-stu-id="562cb-216">PT_I8</span></span>  <br/> |<span data-ttu-id="562cb-217">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="562cb-217">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="562cb-218">Динамические значения</span><span class="sxs-lookup"><span data-stu-id="562cb-218">Dynamic Values</span></span>

<span data-ttu-id="562cb-219">Другие свойства содержат данные в блоке данных значения после первых 16 байтов, включающие тег свойства, зарезервированные данные и объединение значений свойства.</span><span class="sxs-lookup"><span data-stu-id="562cb-219">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="562cb-220">В отличие от статических значений, данные, которые хранятся в 8-байтовом объединении значений свойства иррелевантны при прочтении.</span><span class="sxs-lookup"><span data-stu-id="562cb-220">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="562cb-221">Обеспечьте заполнение 8 байтов данными при записывании.</span><span class="sxs-lookup"><span data-stu-id="562cb-221">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="562cb-222">Содержимое этих 8 байтов не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="562cb-222">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="562cb-223">В случае динамических значений тип тега свойства определяет, как интерпретировать данные значения.</span><span class="sxs-lookup"><span data-stu-id="562cb-223">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="562cb-224">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="562cb-224">PT_STRING8</span></span> 
  
|<span data-ttu-id="562cb-225">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-225">**Value Data**</span></span>|<span data-ttu-id="562cb-226">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-226">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-227">Количество байтов n</span><span class="sxs-lookup"><span data-stu-id="562cb-227">Number of bytes n</span></span>  <br/> |<span data-ttu-id="562cb-228">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-228">4</span></span>  <br/> |
|<span data-ttu-id="562cb-229">Байты, интерпретируемые как строка ANSI (включает знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="562cb-229">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="562cb-230">n</span><span class="sxs-lookup"><span data-stu-id="562cb-230">n</span></span>  <br/> |
   
<span data-ttu-id="562cb-231">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="562cb-231">PT_CLSID</span></span>
  
|<span data-ttu-id="562cb-232">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-232">**Value Data**</span></span>|<span data-ttu-id="562cb-233">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-233">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-234">Байты, интерпретируемые как GUID</span><span class="sxs-lookup"><span data-stu-id="562cb-234">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="562cb-235">16 </span><span class="sxs-lookup"><span data-stu-id="562cb-235">16</span></span>  <br/> |
|||
   
<span data-ttu-id="562cb-236">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="562cb-236">PT_BINARY</span></span> 
  
|<span data-ttu-id="562cb-237">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-237">**Value Data**</span></span>|<span data-ttu-id="562cb-238">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-238">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-239">Количество байтов n</span><span class="sxs-lookup"><span data-stu-id="562cb-239">Number of bytes n</span></span>  <br/> |<span data-ttu-id="562cb-240">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-240">4</span></span>  <br/> |
|<span data-ttu-id="562cb-241">Байты, интерпретируемые как массив байтов</span><span class="sxs-lookup"><span data-stu-id="562cb-241">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="562cb-242">n</span><span class="sxs-lookup"><span data-stu-id="562cb-242">n</span></span>  <br/> |
   
<span data-ttu-id="562cb-243">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="562cb-243">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="562cb-244">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-244">**Value Data**</span></span>|<span data-ttu-id="562cb-245">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-245">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-246">Количество двоичных массивов X</span><span class="sxs-lookup"><span data-stu-id="562cb-246">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="562cb-247">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-247">4</span></span>  <br/> |
|<span data-ttu-id="562cb-248">Последовательность байтов, которая содержит двоичные массивы X.</span><span class="sxs-lookup"><span data-stu-id="562cb-248">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="562cb-249">Каждый массив следует интерпретировать точно так же, как и последовательность байтов PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="562cb-249">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="562cb-250">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-250">Variable</span></span>  <br/> |
   
<span data-ttu-id="562cb-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010 и Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="562cb-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="562cb-252">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-252">**Value Data**</span></span>|<span data-ttu-id="562cb-253">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-253">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-254">Количество строк ANSI X</span><span class="sxs-lookup"><span data-stu-id="562cb-254">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="562cb-255">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-255">4</span></span>  <br/> |
|<span data-ttu-id="562cb-256">Последовательность байтов, которая содержит строки ANSI X.</span><span class="sxs-lookup"><span data-stu-id="562cb-256">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="562cb-257">Каждую строку нужно интерпретировать точно так же, как и последовательность байтов PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="562cb-257">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="562cb-258">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-258">Variable</span></span>  <br/> |
   
<span data-ttu-id="562cb-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="562cb-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="562cb-260">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="562cb-260">**Value Data**</span></span>|<span data-ttu-id="562cb-261">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="562cb-261">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562cb-262">Количество строк Юникода X</span><span class="sxs-lookup"><span data-stu-id="562cb-262">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="562cb-263">4 </span><span class="sxs-lookup"><span data-stu-id="562cb-263">4</span></span>  <br/> |
|<span data-ttu-id="562cb-264">Последовательность байтов, которая содержит строки Юникода X.</span><span class="sxs-lookup"><span data-stu-id="562cb-264">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="562cb-265">Каждую строку нужно интерпретировать точно так же, как и последовательность байтов PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="562cb-265">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="562cb-266">Переменная</span><span class="sxs-lookup"><span data-stu-id="562cb-266">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="562cb-267">Значительные свойства</span><span class="sxs-lookup"><span data-stu-id="562cb-267">Significant properties</span></span>

<span data-ttu-id="562cb-268">Как уже было сказано в этой статье, двоичные блоки, представляющие свойства, имеют теги свойства, которые соответствуют свойствам получателей из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="562cb-268">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="562cb-269">Описание тегов, которые не указаны здесь, вы можете найти в статье https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="562cb-269">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="562cb-270">**Имя свойства**</span><span class="sxs-lookup"><span data-stu-id="562cb-270">**Property Name**</span></span>|<span data-ttu-id="562cb-271">**Тег свойства**</span><span class="sxs-lookup"><span data-stu-id="562cb-271">**Property Tag**</span></span>|<span data-ttu-id="562cb-272">**Описание (дополнительные сведения см. на сайте MSDN)**</span><span class="sxs-lookup"><span data-stu-id="562cb-272">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="562cb-273">PR_NICK_NAME_W (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="562cb-273">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="562cb-274">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="562cb-274">0x6001001f</span></span>  <br/> |<span data-ttu-id="562cb-275">Это свойство должно быть первым в каждой строке получателей.</span><span class="sxs-lookup"><span data-stu-id="562cb-275">This property must be first in each recipient row.</span></span> <span data-ttu-id="562cb-276">Функционально является идентификатором ключа строки получателей.</span><span class="sxs-lookup"><span data-stu-id="562cb-276">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="562cb-277">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="562cb-277">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="562cb-278">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="562cb-278">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="562cb-279">Идентификатор записи адресной книги для получателя.</span><span class="sxs-lookup"><span data-stu-id="562cb-279">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="562cb-280">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="562cb-280">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="562cb-281">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="562cb-281">0x3001001F</span></span>  <br/> |<span data-ttu-id="562cb-282">Отображаемое имя получателя.</span><span class="sxs-lookup"><span data-stu-id="562cb-282">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="562cb-283">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="562cb-283">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="562cb-284">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="562cb-284">0x3003001F</span></span>  <br/> |<span data-ttu-id="562cb-285">Электронный адрес получателя (например, gregoryavdeev@contoso.com или /o=Contoso/OU=Foo/cn=Recipients/cn=gregoryavdeev).</span><span class="sxs-lookup"><span data-stu-id="562cb-285">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="562cb-286">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="562cb-286">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="562cb-287">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="562cb-287">0x3002001F</span></span>  <br/> |<span data-ttu-id="562cb-288">Тип адреса получателя (например, SMTP или EX).</span><span class="sxs-lookup"><span data-stu-id="562cb-288">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="562cb-289">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="562cb-289">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="562cb-290">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="562cb-290">0x300B0102</span></span>  <br/> |<span data-ttu-id="562cb-291">Ключ поиска MAPI получателя.</span><span class="sxs-lookup"><span data-stu-id="562cb-291">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="562cb-292">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="562cb-292">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="562cb-293">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="562cb-293">0x39FE001f</span></span>  <br/> |<span data-ttu-id="562cb-294">SMTP-адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="562cb-294">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="562cb-295">PR_DROPDOWN_DISPLAY_NAME_W (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="562cb-295">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="562cb-296">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="562cb-296">0X6003001f</span></span>  <br/> |<span data-ttu-id="562cb-297">Отображаемая строка, которая появляется в списке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-297">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="562cb-298">PR_NICK_NAME_WEIGHT (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="562cb-298">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="562cb-299">0x60040003</span><span class="sxs-lookup"><span data-stu-id="562cb-299">0x60040003</span></span>  <br/> |<span data-ttu-id="562cb-300">Вес этой записи автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-300">The weight of this autocomplete entry.</span></span> <span data-ttu-id="562cb-301">Вес позволяет определить порядок записей автозаполнения при сопоставлении со списком автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-301">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="562cb-302">Записи с большим весом будут отображаться перед записями с меньшим весом.</span><span class="sxs-lookup"><span data-stu-id="562cb-302">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="562cb-303">Готовый список автозаполнения сортируется согласно этому свойству.</span><span class="sxs-lookup"><span data-stu-id="562cb-303">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="562cb-304">Вес уменьшается с течением времени и увеличивается, когда пользователь отправляет сообщение соответствующему получателю.</span><span class="sxs-lookup"><span data-stu-id="562cb-304">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="562cb-305">Дополнительные сведения об этом свойстве см. далее в статье.</span><span class="sxs-lookup"><span data-stu-id="562cb-305">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="562cb-306">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="562cb-306">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="562cb-307">Набор строк в потоке автозаполнения сортируется в порядке убывания согласно свойству PR_NICK_NAME_WEIGHT. Эта характеристика сортировки всегда должна сохраняться в потоке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="562cb-307">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="562cb-308">Изменения в весе строки должны обеспечивать соответствие ее позиции порядку сортировки в готовом наборе сток.</span><span class="sxs-lookup"><span data-stu-id="562cb-308">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="562cb-309">Возможные дополнительные элементы должны вноситься в наборы строк согласно порядку сортировки.</span><span class="sxs-lookup"><span data-stu-id="562cb-309">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="562cb-310">Минимальное значение веса — 0x1, а максимальное значение — LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="562cb-310">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="562cb-311">Любые другие значения веса считаются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="562cb-311">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="562cb-312">Когда Outlook 2007 сопоставляет получателя или отправляет ему сообщение, вес этого получателя возрастает на 0x2000.</span><span class="sxs-lookup"><span data-stu-id="562cb-312">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

