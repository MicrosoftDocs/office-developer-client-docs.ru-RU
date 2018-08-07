---
title: Структура потока SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812316"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="d2d19-103">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="d2d19-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="d2d19-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2d19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2d19-105">Структура потока SkipBlock — блок данных, который начинается с целое число, указывающее длину оставшихся часть блока.</span><span class="sxs-lookup"><span data-stu-id="d2d19-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="d2d19-106">Эта структура потока существует в потоке [FieldDefinition](fielddefinition-stream-structure.md) Если определение поля в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="d2d19-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="d2d19-107">Назначение структуру потока SkipBlock зависит от его относительно расположения в серии из как структуры в элементе data SkipBlocks FieldDefinition потока.</span><span class="sxs-lookup"><span data-stu-id="d2d19-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="d2d19-108">Серии SkipBlocks должны содержать по крайней мере один SkipBlock структуры, который имеет элемент размер данных, равно 0 и завершает серии.</span><span class="sxs-lookup"><span data-stu-id="d2d19-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="d2d19-109">Если первый структура не прерывающие структура (то есть элемент данных размером больше 0), Outlook предполагается, что первая структура указывает имя поля в кодировке Юникод (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="d2d19-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="d2d19-110">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="d2d19-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="d2d19-111">Размер: Значение DWORD (4 байта), размер, в байтах, элемента данных контента.</span><span class="sxs-lookup"><span data-stu-id="d2d19-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="d2d19-112">Содержимое: Массив БАЙТОВ.</span><span class="sxs-lookup"><span data-stu-id="d2d19-112">Content: An array of BYTE.</span></span> <span data-ttu-id="d2d19-113">Число этого массива равно размер элемента данных.</span><span class="sxs-lookup"><span data-stu-id="d2d19-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="d2d19-114">Значение элемента контента данных зависит от расположения структура SkipBlock из серии и версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2d19-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="d2d19-115">Если первый структуры SkipBlock не прерывающие структуры, Outlook рассматривает первого структура SkipBlock структуры [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) потока, которая указывает имя поля в Юникод.</span><span class="sxs-lookup"><span data-stu-id="d2d19-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d2d19-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d2d19-116">See also</span></span>



[<span data-ttu-id="d2d19-117">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="d2d19-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="d2d19-118">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="d2d19-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d2d19-119">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="d2d19-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="d2d19-120">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="d2d19-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

