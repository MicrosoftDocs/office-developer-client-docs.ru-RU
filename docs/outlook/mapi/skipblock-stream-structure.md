---
title: Структура потока SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580903"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="985da-103">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="985da-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="985da-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="985da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="985da-105">Структура потока SkipBlock — блок данных, который начинается с целое число, указывающее длину оставшихся часть блока.</span><span class="sxs-lookup"><span data-stu-id="985da-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="985da-106">Эта структура потока существует в потоке [FieldDefinition](fielddefinition-stream-structure.md) Если определение поля в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="985da-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="985da-107">Назначение структуру потока SkipBlock зависит от его относительно расположения в серии из как структуры в элементе data SkipBlocks FieldDefinition потока.</span><span class="sxs-lookup"><span data-stu-id="985da-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="985da-108">Серии SkipBlocks должны содержать по крайней мере один SkipBlock структуры, который имеет элемент размер данных, равно 0 и завершает серии.</span><span class="sxs-lookup"><span data-stu-id="985da-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="985da-109">Если первый структура не прерывающие структура (то есть элемент данных размером больше 0), Outlook предполагается, что первая структура указывает имя поля в кодировке Юникод (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="985da-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="985da-110">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="985da-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="985da-111">Размер: Значение DWORD (4 байта), размер, в байтах, элемента данных контента.</span><span class="sxs-lookup"><span data-stu-id="985da-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="985da-112">Содержимое: Массив БАЙТОВ.</span><span class="sxs-lookup"><span data-stu-id="985da-112">Content: An array of BYTE.</span></span> <span data-ttu-id="985da-113">Число этого массива равно размер элемента данных.</span><span class="sxs-lookup"><span data-stu-id="985da-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="985da-114">Значение элемента контента данных зависит от расположения структура SkipBlock из серии и версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="985da-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="985da-115">Если первый структуры SkipBlock не прерывающие структуры, Outlook рассматривает первого структура SkipBlock структуры [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) потока, которая указывает имя поля в Юникод.</span><span class="sxs-lookup"><span data-stu-id="985da-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="985da-116">См. также</span><span class="sxs-lookup"><span data-stu-id="985da-116">See also</span></span>



[<span data-ttu-id="985da-117">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="985da-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="985da-118">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="985da-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="985da-119">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="985da-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="985da-120">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="985da-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

