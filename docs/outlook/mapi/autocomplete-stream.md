---
title: Поток автозаполнения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808108"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="3362c-103">Поток автозаполнения</span><span class="sxs-lookup"><span data-stu-id="3362c-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="3362c-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3362c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3362c-105">В дополнение к информации, как Microsoft Outlook взаимодействует с потоком автозаполнения, необходимо также понять двоичном формате в потоке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3362c-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="3362c-106">Поток автозаполнения представляют собой набор строк получателей свойства, которые сохраняются в виде двоичного потока вместе с некоторые регистрации метаданные, которые используются только в Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 и Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="3362c-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="3362c-107">Метаданные относится к Outlook взаимодействия с потоком автозаполнения, сторонние производители должны сохранить возможности каждого блока метаданных при сохранении измененного автозаполнения потока.</span><span class="sxs-lookup"><span data-stu-id="3362c-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="3362c-108">Другими словами сторонние производители следует изменить только часть набор строк двоичного формата и сохранить Какова была уже в блоков метаданных в потоке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3362c-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="3362c-109">Визуализация потока</span><span class="sxs-lookup"><span data-stu-id="3362c-109">Stream Visualization</span></span>

<span data-ttu-id="3362c-110">Общий макет потока автозаполнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3362c-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="3362c-111">Метаданные (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="3362c-112">Основной номер версии (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="3362c-113">Дополнительный номер версии (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="3362c-114">Количество строк n (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="3362c-115">Число свойств p в первой строке (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="3362c-116">Свойство tag свойство 1 (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="3362c-117">Свойство 1 зарезервировано данных (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="3362c-118">Объединение значение свойства 1 (8 байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="3362c-119">Данные значения свойства 1 (0 или переменной байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="3362c-120">…</span><span class="sxs-lookup"><span data-stu-id="3362c-120"></span></span> <span data-ttu-id="3362c-121">(свойство 2 через свойство P-1)</span><span class="sxs-lookup"><span data-stu-id="3362c-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="3362c-122">Тег свойства свойства элемента p (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="3362c-123">P свойства зарезервировано данных (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="3362c-124">Объединение значение свойства элемента p (8 байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="3362c-125">Данные значения свойства элемента p (0 или переменной байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="3362c-126">Число свойств q в двух строк (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="3362c-127">…</span><span class="sxs-lookup"><span data-stu-id="3362c-127"></span></span> <span data-ttu-id="3362c-128">(строка двух свойств)</span><span class="sxs-lookup"><span data-stu-id="3362c-128">(row two's properties)</span></span>
  
<span data-ttu-id="3362c-129">…</span><span class="sxs-lookup"><span data-stu-id="3362c-129"></span></span> <span data-ttu-id="3362c-130">(3-n-1 строки строка)</span><span class="sxs-lookup"><span data-stu-id="3362c-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="3362c-131">Число свойств r в строку n (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="3362c-132">…</span><span class="sxs-lookup"><span data-stu-id="3362c-132"></span></span> <span data-ttu-id="3362c-133">(строка n's свойств)</span><span class="sxs-lookup"><span data-stu-id="3362c-133">(row n's properties)</span></span>
  
<span data-ttu-id="3362c-134">Дополнительные сведения о число байтов EI (4 байта)</span><span class="sxs-lookup"><span data-stu-id="3362c-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="3362c-135">Дополнительные сведения о (EI байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="3362c-136">Метаданные (8 байт)</span><span class="sxs-lookup"><span data-stu-id="3362c-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="3362c-137">В качестве примера двоичной структуры видеть двоичные примера в [Формат файлов Outlook 2003 и 2007 NK2 и рекомендации разработчикам.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="3362c-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="3362c-138">Высокоуровневая структура</span><span class="sxs-lookup"><span data-stu-id="3362c-138">High-level Layout</span></span>

<span data-ttu-id="3362c-139">Вообще, макета в потоке автозаполнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3362c-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="3362c-140">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-140">**Value Data**</span></span>|<span data-ttu-id="3362c-141">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-142">Метаданные</span><span class="sxs-lookup"><span data-stu-id="3362c-142">Metadata</span></span>  <br/> |<span data-ttu-id="3362c-143">4</span><span class="sxs-lookup"><span data-stu-id="3362c-143">4</span></span>  <br/> |
|<span data-ttu-id="3362c-144">Основной номер версии</span><span class="sxs-lookup"><span data-stu-id="3362c-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="3362c-145">4</span><span class="sxs-lookup"><span data-stu-id="3362c-145">4</span></span>  <br/> |
|<span data-ttu-id="3362c-146">Дополнительный номер версии</span><span class="sxs-lookup"><span data-stu-id="3362c-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="3362c-147">4</span><span class="sxs-lookup"><span data-stu-id="3362c-147">4</span></span>  <br/> |
|<span data-ttu-id="3362c-148">Набор строк</span><span class="sxs-lookup"><span data-stu-id="3362c-148">Row-set</span></span>  <br/> |<span data-ttu-id="3362c-149">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-149">Variable</span></span>  <br/> |
|<span data-ttu-id="3362c-150">Дополнительные сведения о число байтов EI</span><span class="sxs-lookup"><span data-stu-id="3362c-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="3362c-151">4</span><span class="sxs-lookup"><span data-stu-id="3362c-151">4</span></span>  <br/> |
|<span data-ttu-id="3362c-152">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3362c-152">Extra information</span></span>  <br/> |<span data-ttu-id="3362c-153">EI</span><span class="sxs-lookup"><span data-stu-id="3362c-153">EI</span></span>  <br/> |
|<span data-ttu-id="3362c-154">Метаданные</span><span class="sxs-lookup"><span data-stu-id="3362c-154">Metadata</span></span>  <br/> |<span data-ttu-id="3362c-155">8</span><span class="sxs-lookup"><span data-stu-id="3362c-155">8</span></span>  <br/> |
   
<span data-ttu-id="3362c-156">При чтении этого потока, если основной номер версии, отличается от 12, затем этот поток должен не чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="3362c-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="3362c-157">Текущий дополнительный номер версии в потоке автозаполнения — 0, который содержит дополнительные сведения о число байтов значение 0.</span><span class="sxs-lookup"><span data-stu-id="3362c-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="3362c-158">Если дополнительный номер версии, отличается от 0, затем будет сведения в дополнительных сведений, которые необходимо прочитать при чтении потока и сохраняются при записи в поток.</span><span class="sxs-lookup"><span data-stu-id="3362c-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="3362c-159">Дополнительный номер версии будет также должны сохраняться при записи в поток.</span><span class="sxs-lookup"><span data-stu-id="3362c-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="3362c-160">Если они не сохраняются, данные будут потеряны экземпляры Outlook, который был создан дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="3362c-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3362c-161">Приложения не следует добавлять пользовательские данные в поле Дополнительные сведения или изменить дополнительный номер версии, как эти функциональные возможности для поддержки расширения Outlook до формата и не произвольных extensions сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="3362c-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="3362c-162">Макет набор строк</span><span class="sxs-lookup"><span data-stu-id="3362c-162">Row-set Layout</span></span>

<span data-ttu-id="3362c-163">Макет набор строк выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3362c-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="3362c-164">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-164">**Value Data**</span></span>|<span data-ttu-id="3362c-165">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-166">Количество строк</span><span class="sxs-lookup"><span data-stu-id="3362c-166">Number of rows</span></span>  <br/> |<span data-ttu-id="3362c-167">4</span><span class="sxs-lookup"><span data-stu-id="3362c-167">4</span></span>  <br/> |
|<span data-ttu-id="3362c-168">Rows</span><span class="sxs-lookup"><span data-stu-id="3362c-168">Rows</span></span>  <br/> |<span data-ttu-id="3362c-169">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="3362c-170">Количество строк определяет, сколько строк поступают в следующей части последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="3362c-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="3362c-171">Макет строк</span><span class="sxs-lookup"><span data-stu-id="3362c-171">Row Layout</span></span>

<span data-ttu-id="3362c-172">Каждая строка имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="3362c-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="3362c-173">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-173">**Value Data**</span></span>|<span data-ttu-id="3362c-174">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-175">Число свойств</span><span class="sxs-lookup"><span data-stu-id="3362c-175">Number of properties</span></span>  <br/> |<span data-ttu-id="3362c-176">4</span><span class="sxs-lookup"><span data-stu-id="3362c-176">4</span></span>  <br/> |
|<span data-ttu-id="3362c-177">Свойства</span><span class="sxs-lookup"><span data-stu-id="3362c-177">Properties</span></span>  <br/> |<span data-ttu-id="3362c-178">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="3362c-179">Число свойств определяет, сколько свойства поступают в следующей части последовательности двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="3362c-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="3362c-180">Свойство макета</span><span class="sxs-lookup"><span data-stu-id="3362c-180">Property Layout</span></span>

<span data-ttu-id="3362c-181">Каждое свойство имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="3362c-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="3362c-182">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-182">**Value Data**</span></span>|<span data-ttu-id="3362c-183">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-184">Свойство Tag</span><span class="sxs-lookup"><span data-stu-id="3362c-184">Property Tag</span></span>  <br/> |<span data-ttu-id="3362c-185">4</span><span class="sxs-lookup"><span data-stu-id="3362c-185">4</span></span>  <br/> |
|<span data-ttu-id="3362c-186">Зарезервированные данных</span><span class="sxs-lookup"><span data-stu-id="3362c-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="3362c-187">4</span><span class="sxs-lookup"><span data-stu-id="3362c-187">4</span></span>  <br/> |
|<span data-ttu-id="3362c-188">Объединение значение свойства</span><span class="sxs-lookup"><span data-stu-id="3362c-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="3362c-189">Данные значения</span><span class="sxs-lookup"><span data-stu-id="3362c-189">Value Data</span></span>  <br/> |<span data-ttu-id="3362c-190">0 или переменной (в зависимости от свойства tag)</span><span class="sxs-lookup"><span data-stu-id="3362c-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="3362c-191">Интерпретация значения свойства</span><span class="sxs-lookup"><span data-stu-id="3362c-191">Interpreting the Property Value</span></span>

<span data-ttu-id="3362c-192">Объединение значение свойства и значения, воспринимается на основе свойства тега в первые 4 байта в блоке свойство.</span><span class="sxs-lookup"><span data-stu-id="3362c-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="3362c-193">Этот тег свойства — в виде тега свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="3362c-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="3362c-194">Цифры от 0 до 15 тега свойства биты типа свойства.</span><span class="sxs-lookup"><span data-stu-id="3362c-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="3362c-195">16 до 31 биты идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="3362c-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="3362c-196">Тип свойства определяет, как следует прочитать остальные свойства.</span><span class="sxs-lookup"><span data-stu-id="3362c-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="3362c-197">Статическое значение</span><span class="sxs-lookup"><span data-stu-id="3362c-197">Static Value</span></span>

<span data-ttu-id="3362c-198">Некоторые свойства, не имеющие значение данных и только данные в объединение.</span><span class="sxs-lookup"><span data-stu-id="3362c-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="3362c-199">Следующие типы свойств (которые поступают из свойства Tag) следует воспринимать свойство объединения данных 8 байтов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3362c-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="3362c-200">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="3362c-200">**Prop Type**</span></span>|<span data-ttu-id="3362c-201">**Свойство объединения Интерпретация**</span><span class="sxs-lookup"><span data-stu-id="3362c-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="3362c-202">PT_I2</span></span>  <br/> |<span data-ttu-id="3362c-203">короткое целое</span><span class="sxs-lookup"><span data-stu-id="3362c-203">short int</span></span>  <br/> |
|<span data-ttu-id="3362c-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3362c-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="3362c-205">длинный</span><span class="sxs-lookup"><span data-stu-id="3362c-205">long</span></span>  <br/> |
|<span data-ttu-id="3362c-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="3362c-206">PT_R4</span></span>  <br/> |<span data-ttu-id="3362c-207">с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="3362c-207">float</span></span>  <br/> |
|<span data-ttu-id="3362c-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="3362c-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="3362c-209">double</span><span class="sxs-lookup"><span data-stu-id="3362c-209">double</span></span>  <br/> |
|<span data-ttu-id="3362c-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3362c-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="3362c-211">короткое целое</span><span class="sxs-lookup"><span data-stu-id="3362c-211">short int</span></span>  <br/> |
|<span data-ttu-id="3362c-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3362c-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="3362c-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="3362c-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="3362c-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="3362c-214">PT_I8</span></span>  <br/> |<span data-ttu-id="3362c-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="3362c-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="3362c-216">Динамические значения</span><span class="sxs-lookup"><span data-stu-id="3362c-216">Dynamic Values</span></span>

<span data-ttu-id="3362c-217">Другие свойства содержат данные в блоке значение данных после первого 16 байтов, которые содержат тег свойства, зарезервированные данные и объединения значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3362c-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="3362c-218">В отличие от статического значения данные, которые хранятся в союзе 8-байтовое значение свойства не имеет значения для чтения.</span><span class="sxs-lookup"><span data-stu-id="3362c-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="3362c-219">При создании, убедитесь в том, заполните следующие 8 байтов с что-то.</span><span class="sxs-lookup"><span data-stu-id="3362c-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="3362c-220">Тем не менее содержимое 8 байтов не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="3362c-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="3362c-221">В динамической значения тип тега свойства определяет, как интерпретировать данные значения.</span><span class="sxs-lookup"><span data-stu-id="3362c-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="3362c-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3362c-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="3362c-223">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-223">**Value Data**</span></span>|<span data-ttu-id="3362c-224">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-225">Число байт n</span><span class="sxs-lookup"><span data-stu-id="3362c-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="3362c-226">4</span><span class="sxs-lookup"><span data-stu-id="3362c-226">4</span></span>  <br/> |
|<span data-ttu-id="3362c-227">Байт в виде строки ANSI (включая символ конца строки)</span><span class="sxs-lookup"><span data-stu-id="3362c-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="3362c-228">n</span><span class="sxs-lookup"><span data-stu-id="3362c-228">n</span></span>  <br/> |
   
<span data-ttu-id="3362c-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="3362c-229">PT_CLSID</span></span>
  
|<span data-ttu-id="3362c-230">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-230">**Value Data**</span></span>|<span data-ttu-id="3362c-231">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-232">Байт воспринимается как код GUID</span><span class="sxs-lookup"><span data-stu-id="3362c-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="3362c-233">16</span><span class="sxs-lookup"><span data-stu-id="3362c-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="3362c-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3362c-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="3362c-235">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-235">**Value Data**</span></span>|<span data-ttu-id="3362c-236">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-237">Число байт n</span><span class="sxs-lookup"><span data-stu-id="3362c-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="3362c-238">4</span><span class="sxs-lookup"><span data-stu-id="3362c-238">4</span></span>  <br/> |
|<span data-ttu-id="3362c-239">Байт в виде массива байтов</span><span class="sxs-lookup"><span data-stu-id="3362c-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="3362c-240">n</span><span class="sxs-lookup"><span data-stu-id="3362c-240">n</span></span>  <br/> |
   
<span data-ttu-id="3362c-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="3362c-241">PT_ERROR</span></span>
  
|<span data-ttu-id="3362c-242">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-242">**Value Data**</span></span>|<span data-ttu-id="3362c-243">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-244">Число байт n</span><span class="sxs-lookup"><span data-stu-id="3362c-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="3362c-245">4</span><span class="sxs-lookup"><span data-stu-id="3362c-245">4</span></span>  <br/> |
|<span data-ttu-id="3362c-246">Байт в виде массива байтов</span><span class="sxs-lookup"><span data-stu-id="3362c-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="3362c-247">n</span><span class="sxs-lookup"><span data-stu-id="3362c-247">n</span></span>  <br/> |
   
<span data-ttu-id="3362c-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3362c-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="3362c-249">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-249">**Value Data**</span></span>|<span data-ttu-id="3362c-250">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-251">Количество двоичных массивов X</span><span class="sxs-lookup"><span data-stu-id="3362c-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="3362c-252">4</span><span class="sxs-lookup"><span data-stu-id="3362c-252">4</span></span>  <br/> |
|<span data-ttu-id="3362c-253">Запустите A байтов, которые содержит X двоичные массивов.</span><span class="sxs-lookup"><span data-stu-id="3362c-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="3362c-254">Каждый массив интерпретации так же, как запустить PT_BINARY байт.</span><span class="sxs-lookup"><span data-stu-id="3362c-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="3362c-255">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="3362c-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010 и Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="3362c-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="3362c-257">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-257">**Value Data**</span></span>|<span data-ttu-id="3362c-258">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-259">Количество строк ANSI X</span><span class="sxs-lookup"><span data-stu-id="3362c-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="3362c-260">4</span><span class="sxs-lookup"><span data-stu-id="3362c-260">4</span></span>  <br/> |
|<span data-ttu-id="3362c-261">Запуск байтов, который содержит строки X ANSI.</span><span class="sxs-lookup"><span data-stu-id="3362c-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="3362c-262">Каждая строка интерпретации так же, как запустить PT_STRING8 байт.</span><span class="sxs-lookup"><span data-stu-id="3362c-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="3362c-263">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="3362c-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="3362c-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="3362c-265">**Данные значения**</span><span class="sxs-lookup"><span data-stu-id="3362c-265">**Value Data**</span></span>|<span data-ttu-id="3362c-266">**Число байт**</span><span class="sxs-lookup"><span data-stu-id="3362c-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3362c-267">Количество строк в кодировке Юникод X</span><span class="sxs-lookup"><span data-stu-id="3362c-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="3362c-268">4</span><span class="sxs-lookup"><span data-stu-id="3362c-268">4</span></span>  <br/> |
|<span data-ttu-id="3362c-269">Запуск байтов, который содержит X UNICODE строк.</span><span class="sxs-lookup"><span data-stu-id="3362c-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="3362c-270">Каждая строка интерпретации так же, как запустить PT_UNICODE байт.</span><span class="sxs-lookup"><span data-stu-id="3362c-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="3362c-271">Переменная</span><span class="sxs-lookup"><span data-stu-id="3362c-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="3362c-272">Значительные свойства</span><span class="sxs-lookup"><span data-stu-id="3362c-272">Significant properties</span></span>

<span data-ttu-id="3362c-273">Как упоминалось ранее в этом разделе, двоичные блоки, представляющих свойства имеют теги свойства, которые соответствуют свойствам получателей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3362c-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="3362c-274">Для свойств, не перечисленных здесь, можно найти в описании свойства в http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="3362c-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="3362c-275">**Имя свойства**</span><span class="sxs-lookup"><span data-stu-id="3362c-275">**Property Name**</span></span>|<span data-ttu-id="3362c-276">**Свойство Tag**</span><span class="sxs-lookup"><span data-stu-id="3362c-276">**Property Tag**</span></span>|<span data-ttu-id="3362c-277">**Описание (Дополнительные сведения см MSDN)**</span><span class="sxs-lookup"><span data-stu-id="3362c-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3362c-278">PR_NICK_NAME_W (не передаются на получателей, специально для потока автозаполнения только)</span><span class="sxs-lookup"><span data-stu-id="3362c-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="3362c-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="3362c-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="3362c-280">Это свойство должно быть первым в каждой строке получателя.</span><span class="sxs-lookup"><span data-stu-id="3362c-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="3362c-281">Функционально служит в качестве идентификатор ключа для строки получателей.</span><span class="sxs-lookup"><span data-stu-id="3362c-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="3362c-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3362c-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="3362c-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="3362c-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="3362c-284">Идентификатор записи книги адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="3362c-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="3362c-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3362c-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="3362c-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="3362c-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="3362c-287">Отображаемое имя получателя.</span><span class="sxs-lookup"><span data-stu-id="3362c-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="3362c-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="3362c-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="3362c-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="3362c-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="3362c-290">Адрес электронной почты получателя (например, johndoe@contoso.com или/o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)</span><span class="sxs-lookup"><span data-stu-id="3362c-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="3362c-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="3362c-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="3362c-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="3362c-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="3362c-293">Тип адреса получателя (например, SMTP или EX).</span><span class="sxs-lookup"><span data-stu-id="3362c-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="3362c-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="3362c-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="3362c-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="3362c-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="3362c-296">Ключ поиска MAPI получателя.</span><span class="sxs-lookup"><span data-stu-id="3362c-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="3362c-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="3362c-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="3362c-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="3362c-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="3362c-299">SMTP-адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="3362c-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="3362c-300">PR_DROPDOWN_DISPLAY_NAME_W (не передаются на получателей, специально для потока автозаполнения только)</span><span class="sxs-lookup"><span data-stu-id="3362c-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="3362c-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="3362c-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="3362c-302">Строка отображения, который отображается в списке автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3362c-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="3362c-303">PR_NICK_NAME_WEIGHT (не передаются на получателей, специально для потока автозаполнения только)</span><span class="sxs-lookup"><span data-stu-id="3362c-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="3362c-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="3362c-304">0x60040003</span></span>  <br/> |<span data-ttu-id="3362c-305">Вес в этой записи автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3362c-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="3362c-306">Вес используется для определения, в какой автозаполнения порядке записи возникают при анализе списки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3362c-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="3362c-307">Операции с более высоким вес будут отображаться перед операции с нижней вес.</span><span class="sxs-lookup"><span data-stu-id="3362c-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="3362c-308">Список завершения автозаполнения сортируется этим свойством.</span><span class="sxs-lookup"><span data-stu-id="3362c-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="3362c-309">Вес периодически снижает по времени и увеличивается, когда пользователь отправляет сообщение электронной почты данному получателю.</span><span class="sxs-lookup"><span data-stu-id="3362c-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="3362c-310">В разделе Описание далее в данном разделе приведены дополнительные сведения об этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="3362c-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="3362c-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="3362c-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="3362c-312">Набор строк в потоке автозаполнения сортируются в порядке убывания свойством PR_NICK_NAME_WEIGHT и потока автозаполнения всегда должен сохранить этот отсортированный характеристики.</span><span class="sxs-lookup"><span data-stu-id="3362c-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="3362c-313">Таким образом любые изменения строки вес необходимо убедиться, что строка содержит порядок сортировки полный набор строк.</span><span class="sxs-lookup"><span data-stu-id="3362c-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="3362c-314">Любые добавления к набор строк вставляется в правильное положение на обслуживание порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="3362c-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="3362c-315">Минимальное значение в этом вес является 0x1 и максимальное значение — LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="3362c-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="3362c-316">Все значения для него значение считается недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="3362c-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="3362c-317">Когда отправляет почты в Outlook 2007 или разрешается получателя, он будет увеличен вес, получатель 0x2000.</span><span class="sxs-lookup"><span data-stu-id="3362c-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

