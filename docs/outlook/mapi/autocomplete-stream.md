---
title: Поток автозаполнения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b5c5fee71db0fc7bdd6e01c58e9c9a9c3d9fa22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318083"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="bfbcb-103">Поток автозаполнения</span><span class="sxs-lookup"><span data-stu-id="bfbcb-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="bfbcb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfbcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfbcb-105">Необходимо понимать не только то, как Microsoft Outlook взаимодействует с потоком автозаполнения, но и двоичный формат потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="bfbcb-106">Поток автозаполнения — это набор строк свойств получателя, который сохраняется в виде двоичного потока вместе с некоторыми метаданными, которые используются только Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 и Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="bfbcb-107">Метаданные относятся к взаимодействиям Outlook с потоком автозаполнения, поэтому третьим сторонам необходимо сохранять содержимое каждого блока метаданных при сохранении измененного потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="bfbcb-108">Иными словами, третьим сторонам следует изменить только часть с набором строк двоичного формата и сохранить изначальное содержимое блока метаданных для потока автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="bfbcb-109">Визуализация потока</span><span class="sxs-lookup"><span data-stu-id="bfbcb-109">Stream Visualization</span></span>

<span data-ttu-id="bfbcb-110">Высокоуровневая структура потока автозаполнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bfbcb-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="bfbcb-111">метаданные (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-112">основной номер версии (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-113">дополнительный номер версии (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-114">количество строк n (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-115">количество свойств p в первой строке (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-116">тег свойства 1 (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-117">зарезервированные данные свойства 1 (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-118">объединение значений для свойства 1 (8 байтов);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="bfbcb-119">данные значения свойства 1 (байты переменной или 0);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="bfbcb-120">…</span><span class="sxs-lookup"><span data-stu-id="bfbcb-120"></span></span> <span data-ttu-id="bfbcb-121">свойства (от свойства 2 до свойства P-1);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="bfbcb-122">тег свойства p (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-123">зарезервированные данные свойства p (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-124">объединение значений для свойства p (8 байтов);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="bfbcb-125">данные значения свойства p (байты переменной или 0);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="bfbcb-126">количество свойств q в строке второй (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-127">…</span><span class="sxs-lookup"><span data-stu-id="bfbcb-127"></span></span> <span data-ttu-id="bfbcb-128">свойства строки второй;</span><span class="sxs-lookup"><span data-stu-id="bfbcb-128">(row two's properties)</span></span>
  
<span data-ttu-id="bfbcb-129">…</span><span class="sxs-lookup"><span data-stu-id="bfbcb-129"></span></span> <span data-ttu-id="bfbcb-130">строки (от строки 3 до строки n-1);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="bfbcb-131">количество свойств r в строке n (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-132">…</span><span class="sxs-lookup"><span data-stu-id="bfbcb-132"></span></span> <span data-ttu-id="bfbcb-133">свойства строки n;</span><span class="sxs-lookup"><span data-stu-id="bfbcb-133">(row n's properties)</span></span>
  
<span data-ttu-id="bfbcb-134">количество байтов дополнительных сведений EI (4 байта);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="bfbcb-135">дополнительные сведения (байты EI);</span><span class="sxs-lookup"><span data-stu-id="bfbcb-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="bfbcb-136">метаданные (8 байтов).</span><span class="sxs-lookup"><span data-stu-id="bfbcb-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="bfbcb-137">Пример двоичной структуры см. в разделе "Binary Example" (Пример двоичной структуры) документа [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf) (Рекомендации разработчикам и сведения о формате NK2 файлов Outlook 2003/2007).</span><span class="sxs-lookup"><span data-stu-id="bfbcb-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="bfbcb-138">Высокоуровневая структура</span><span class="sxs-lookup"><span data-stu-id="bfbcb-138">High-level Layout</span></span>

<span data-ttu-id="bfbcb-139">В целом структура потока автозаполнения выглядит указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="bfbcb-140">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-140">**Value Data**</span></span>|<span data-ttu-id="bfbcb-141">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-142">Метаданные</span><span class="sxs-lookup"><span data-stu-id="bfbcb-142">Metadata</span></span>  <br/> |<span data-ttu-id="bfbcb-143">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-143">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-144">Основной номер версии</span><span class="sxs-lookup"><span data-stu-id="bfbcb-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="bfbcb-145">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-145">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-146">Дополнительный номер версии</span><span class="sxs-lookup"><span data-stu-id="bfbcb-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="bfbcb-147">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-147">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-148">Набор строк</span><span class="sxs-lookup"><span data-stu-id="bfbcb-148">Row-set</span></span>  <br/> |<span data-ttu-id="bfbcb-149">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-149">Variable</span></span>  <br/> |
|<span data-ttu-id="bfbcb-150">Количество байтов дополнительных сведений EI</span><span class="sxs-lookup"><span data-stu-id="bfbcb-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="bfbcb-151">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-151">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-152">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="bfbcb-152">Extra information</span></span>  <br/> |<span data-ttu-id="bfbcb-153">EI</span><span class="sxs-lookup"><span data-stu-id="bfbcb-153">EI</span></span>  <br/> |
|<span data-ttu-id="bfbcb-154">Метаданные</span><span class="sxs-lookup"><span data-stu-id="bfbcb-154">Metadata</span></span>  <br/> |<span data-ttu-id="bfbcb-155">8,5</span><span class="sxs-lookup"><span data-stu-id="bfbcb-155">8</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-156">Если при чтении потока обнаружено, что основной номер версии отличается от 12, то этот поток не следует читать или же записывать.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="bfbcb-157">Текущий дополнительный номер версии потока автозаполнения — 0, то есть количество байтов дополнительной информации равно 0.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="bfbcb-158">Если дополнительный номер версии отличается от 0, то будет присутствовать дополнительная информация, которую необходимо прочесть во время чтения потока и сохранить при записывании потока.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="bfbcb-159">Кроме того, при записывании потока необходимо будет сохранить дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="bfbcb-160">Если не сохранить ни одно из этих значений, данные в записавших дополнительную информацию экземплярах Outlook будут утеряны.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bfbcb-161">Приложения не должны добавлять пользовательские данные в поле дополнительной информации и менять дополнительный номер версии, так как эта функциональность предназначена для поддержки расширений формата для Outlook, а не произвольных сторонних расширений.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="bfbcb-162">Структура набора строк</span><span class="sxs-lookup"><span data-stu-id="bfbcb-162">Row-set Layout</span></span>

<span data-ttu-id="bfbcb-163">Структура набора строк выглядит указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="bfbcb-164">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-164">**Value Data**</span></span>|<span data-ttu-id="bfbcb-165">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-166">Количество строк</span><span class="sxs-lookup"><span data-stu-id="bfbcb-166">Number of rows</span></span>  <br/> |<span data-ttu-id="bfbcb-167">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-167">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-168">Строки</span><span class="sxs-lookup"><span data-stu-id="bfbcb-168">Rows</span></span>  <br/> |<span data-ttu-id="bfbcb-169">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-170">Количество строк определяет, сколько строк попадает в следующую часть последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="bfbcb-171">Структура строки</span><span class="sxs-lookup"><span data-stu-id="bfbcb-171">Row Layout</span></span>

<span data-ttu-id="bfbcb-172">Каждая строка имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="bfbcb-173">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-173">**Value Data**</span></span>|<span data-ttu-id="bfbcb-174">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-175">Количество свойств</span><span class="sxs-lookup"><span data-stu-id="bfbcb-175">Number of properties</span></span>  <br/> |<span data-ttu-id="bfbcb-176">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-176">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-177">Свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-177">Properties</span></span>  <br/> |<span data-ttu-id="bfbcb-178">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-179">Количество свойств определяет, сколько свойств попадает в следующую часть последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="bfbcb-180">Структура свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-180">Property Layout</span></span>

<span data-ttu-id="bfbcb-181">Каждое свойство имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="bfbcb-182">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-182">**Value Data**</span></span>|<span data-ttu-id="bfbcb-183">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-184">Тег свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-184">Property Tag</span></span>  <br/> |<span data-ttu-id="bfbcb-185">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-185">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-186">Зарезервированные данные</span><span class="sxs-lookup"><span data-stu-id="bfbcb-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="bfbcb-187">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-187">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-188">Объединение значений свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="bfbcb-189">Данные значения</span><span class="sxs-lookup"><span data-stu-id="bfbcb-189">Value Data</span></span>  <br/> |<span data-ttu-id="bfbcb-190">0 или переменная (в зависимости от тега свойства)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="bfbcb-191">Интерпретация значения свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-191">Interpreting the Property Value</span></span>

<span data-ttu-id="bfbcb-192">Объединение значений свойства и данные значения следует интерпретировать с учетом тега свойства в первых 4 байтах блока свойства.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="bfbcb-193">У этого тега свойства такой же формат, как и у тега свойства в MAPI.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="bfbcb-194">Биты от 0 до 15 тега свойства соответствуют типу свойства.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="bfbcb-195">Биты от 16 до 31 соответствуют идентификатору свойства.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="bfbcb-196">Тип свойства определяет, как следует читать остальные данные свойства.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="bfbcb-197">Статическое значение</span><span class="sxs-lookup"><span data-stu-id="bfbcb-197">Static Value</span></span>

<span data-ttu-id="bfbcb-198">Некоторые свойства не имеют данных значения, у них есть только данные объединения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="bfbcb-199">Ниже показано, как для типов свойств, которые следуют из тега свойства, должны интерпретироваться 8-байтовые данные объединения свойств.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="bfbcb-200">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-200">**Prop Type**</span></span>|<span data-ttu-id="bfbcb-201">**Интерпретация объединения свойств**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="bfbcb-202">PT_I2</span></span>  <br/> |<span data-ttu-id="bfbcb-203">short int</span><span class="sxs-lookup"><span data-stu-id="bfbcb-203">short int</span></span>  <br/> |
|<span data-ttu-id="bfbcb-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bfbcb-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="bfbcb-205">long</span><span class="sxs-lookup"><span data-stu-id="bfbcb-205">long</span></span>  <br/> |
|<span data-ttu-id="bfbcb-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-206">PT_R4</span></span>  <br/> |<span data-ttu-id="bfbcb-207">float</span><span class="sxs-lookup"><span data-stu-id="bfbcb-207">float</span></span>  <br/> |
|<span data-ttu-id="bfbcb-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="bfbcb-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="bfbcb-209">double</span><span class="sxs-lookup"><span data-stu-id="bfbcb-209">double</span></span>  <br/> |
|<span data-ttu-id="bfbcb-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bfbcb-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="bfbcb-211">short int</span><span class="sxs-lookup"><span data-stu-id="bfbcb-211">short int</span></span>  <br/> |
|<span data-ttu-id="bfbcb-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bfbcb-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="bfbcb-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="bfbcb-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="bfbcb-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="bfbcb-214">PT_I8</span></span>  <br/> |<span data-ttu-id="bfbcb-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="bfbcb-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="bfbcb-216">Динамические значения</span><span class="sxs-lookup"><span data-stu-id="bfbcb-216">Dynamic Values</span></span>

<span data-ttu-id="bfbcb-217">Другие свойства содержат данные в блоке данных значения после первых 16 байтов, включающие тег свойства, зарезервированные данные и объединение значений свойства.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="bfbcb-218">В отличие от статических значений, данные, которые хранятся в 8-байтовом объединении значений свойства иррелевантны при прочтении.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="bfbcb-219">Обеспечьте заполнение 8 байтов данными при записывании.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="bfbcb-220">Содержимое этих 8 байтов не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="bfbcb-221">В случае динамических значений тип тега свойства определяет, как интерпретировать данные значения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="bfbcb-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bfbcb-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="bfbcb-223">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-223">**Value Data**</span></span>|<span data-ttu-id="bfbcb-224">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-225">Количество байтов n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="bfbcb-226">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-226">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-227">Байты, интерпретируемые как строка ANSI (включает знак завершения NULL)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="bfbcb-228">n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-228">n</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="bfbcb-229">PT_CLSID</span></span>
  
|<span data-ttu-id="bfbcb-230">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-230">**Value Data**</span></span>|<span data-ttu-id="bfbcb-231">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-232">Байты, интерпретируемые как GUID</span><span class="sxs-lookup"><span data-stu-id="bfbcb-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="bfbcb-233">столбцов</span><span class="sxs-lookup"><span data-stu-id="bfbcb-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="bfbcb-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfbcb-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="bfbcb-235">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-235">**Value Data**</span></span>|<span data-ttu-id="bfbcb-236">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-237">Количество байтов n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="bfbcb-238">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-238">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-239">Байты, интерпретируемые как массив байтов</span><span class="sxs-lookup"><span data-stu-id="bfbcb-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="bfbcb-240">n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-240">n</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="bfbcb-241">PT_ERROR</span></span>
  
|<span data-ttu-id="bfbcb-242">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-242">**Value Data**</span></span>|<span data-ttu-id="bfbcb-243">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-244">Количество байтов n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="bfbcb-245">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-245">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-246">Байты, интерпретируемые как массив байтов</span><span class="sxs-lookup"><span data-stu-id="bfbcb-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="bfbcb-247">n</span><span class="sxs-lookup"><span data-stu-id="bfbcb-247">n</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfbcb-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="bfbcb-249">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-249">**Value Data**</span></span>|<span data-ttu-id="bfbcb-250">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-251">Количество двоичных массивов X</span><span class="sxs-lookup"><span data-stu-id="bfbcb-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="bfbcb-252">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-252">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-253">Последовательность байтов, которая содержит двоичные массивы X.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="bfbcb-254">Каждый массив следует интерпретировать точно так же, как и последовательность байтов PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="bfbcb-255">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010 и Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="bfbcb-257">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-257">**Value Data**</span></span>|<span data-ttu-id="bfbcb-258">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-259">Количество строк ANSI X</span><span class="sxs-lookup"><span data-stu-id="bfbcb-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="bfbcb-260">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-260">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-261">Последовательность байтов, которая содержит строки ANSI X.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="bfbcb-262">Каждую строку нужно интерпретировать точно так же, как и последовательность байтов PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="bfbcb-263">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="bfbcb-265">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-265">**Value Data**</span></span>|<span data-ttu-id="bfbcb-266">**Количество байтов**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfbcb-267">Количество строк Юникода X</span><span class="sxs-lookup"><span data-stu-id="bfbcb-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="bfbcb-268">SP4</span><span class="sxs-lookup"><span data-stu-id="bfbcb-268">4</span></span>  <br/> |
|<span data-ttu-id="bfbcb-269">Последовательность байтов, которая содержит строки Юникода X.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="bfbcb-270">Каждую строку нужно интерпретировать точно так же, как и последовательность байтов PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="bfbcb-271">Переменная</span><span class="sxs-lookup"><span data-stu-id="bfbcb-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="bfbcb-272">Значительные свойства</span><span class="sxs-lookup"><span data-stu-id="bfbcb-272">Significant properties</span></span>

<span data-ttu-id="bfbcb-273">Как уже было сказано в этой статье, двоичные блоки, представляющие свойства, имеют теги свойства, которые соответствуют свойствам получателей из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="bfbcb-274">Описание тегов, которые не указаны здесь, вы можете найти в статье https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-274">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="bfbcb-275">**Имя свойства**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-275">**Property Name**</span></span>|<span data-ttu-id="bfbcb-276">**Тег свойства**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-276">**Property Tag**</span></span>|<span data-ttu-id="bfbcb-277">**Описание (дополнительные сведения см. на сайте MSDN)**</span><span class="sxs-lookup"><span data-stu-id="bfbcb-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfbcb-278">PR_NICK_NAME_W (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="bfbcb-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="bfbcb-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="bfbcb-280">Это свойство должно быть первым в каждой строке получателей.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="bfbcb-281">Функционально является идентификатором ключа строки получателей.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bfbcb-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="bfbcb-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="bfbcb-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="bfbcb-284">Идентификатор записи адресной книги для получателя.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="bfbcb-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="bfbcb-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="bfbcb-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="bfbcb-287">Отображаемое имя получателя.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="bfbcb-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="bfbcb-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="bfbcb-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="bfbcb-290">Электронный адрес получателя (например, gregoryavdeev@contoso.com или /o=Contoso/OU=Foo/cn=Recipients/cn=gregoryavdeev).</span><span class="sxs-lookup"><span data-stu-id="bfbcb-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="bfbcb-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="bfbcb-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="bfbcb-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="bfbcb-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="bfbcb-293">Тип адреса получателя (например, SMTP или EX).</span><span class="sxs-lookup"><span data-stu-id="bfbcb-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="bfbcb-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bfbcb-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="bfbcb-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="bfbcb-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="bfbcb-296">Ключ поиска MAPI получателя.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="bfbcb-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="bfbcb-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="bfbcb-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="bfbcb-299">SMTP-адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-300">PR_DROPDOWN_DISPLAY_NAME_W (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="bfbcb-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="bfbcb-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="bfbcb-302">Отображаемая строка, которая появляется в списке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="bfbcb-303">PR_NICK_NAME_WEIGHT (не передается получателям, относится только к потоку автозаполнения)</span><span class="sxs-lookup"><span data-stu-id="bfbcb-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="bfbcb-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="bfbcb-304">0x60040003</span></span>  <br/> |<span data-ttu-id="bfbcb-305">Вес этой записи автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="bfbcb-306">Вес позволяет определить порядок записей автозаполнения при сопоставлении со списком автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="bfbcb-307">Записи с большим весом будут отображаться перед записями с меньшим весом.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="bfbcb-308">Готовый список автозаполнения сортируется согласно этому свойству.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="bfbcb-309">Вес уменьшается с течением времени и увеличивается, когда пользователь отправляет сообщение соответствующему получателю.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="bfbcb-310">Дополнительные сведения об этом свойстве см. далее в статье.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="bfbcb-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="bfbcb-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="bfbcb-312">Набор строк в потоке автозаполнения сортируется в порядке убывания согласно свойству PR_NICK_NAME_WEIGHT. Эта характеристика сортировки всегда должна сохраняться в потоке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="bfbcb-313">Изменения в весе строки должны обеспечивать соответствие ее позиции порядку сортировки в готовом наборе сток.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="bfbcb-314">Возможные дополнительные элементы должны вноситься в наборы строк согласно порядку сортировки.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="bfbcb-315">Минимальное значение веса — 0x1, а максимальное значение — LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="bfbcb-316">Любые другие значения веса считаются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="bfbcb-317">Когда Outlook 2007 сопоставляет получателя или отправляет ему сообщение, вес этого получателя возрастает на 0x2000.</span><span class="sxs-lookup"><span data-stu-id="bfbcb-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

