---
title: Структура потока SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435546"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="dcc66-103">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="dcc66-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="dcc66-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcc66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcc66-105">Структура потока SkipBlock — это блок данных, начинающийся с целого числа, который указывает длину оставшейся части блока.</span><span class="sxs-lookup"><span data-stu-id="dcc66-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="dcc66-106">Эта структура потоков существует в потоке [FieldDefinition](fielddefinition-stream-structure.md) , если определение поля находится в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="dcc66-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="dcc66-107">Цель структуры потока SkipBlock зависит от относительного расположения в ряде похожих структур в элементе данных Скипблоккс потока FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="dcc66-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="dcc66-108">Ряд Скипблоккс должен содержать по крайней мере одну структуру SkipBlock, которая завершает ряд и имеет элемент данных size, равный 0.</span><span class="sxs-lookup"><span data-stu-id="dcc66-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="dcc66-109">Если первая структура не является завершающей (то есть элемент данных size больше 0), то предполагается, что первая структура указывает имя поля в Юникоде (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="dcc66-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="dcc66-110">Элементы данных в этом потоке хранятся в порядке байтов с прямым порядком байтов, сразу после друг друга в порядке, указанном ниже.</span><span class="sxs-lookup"><span data-stu-id="dcc66-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="dcc66-111">Size: DWORD (4 байта), размер элемента данных контента (в байтах).</span><span class="sxs-lookup"><span data-stu-id="dcc66-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="dcc66-112">Контент: массив БАЙТОВ.</span><span class="sxs-lookup"><span data-stu-id="dcc66-112">Content: An array of BYTE.</span></span> <span data-ttu-id="dcc66-113">Количество этого массива равно элементу данных size.</span><span class="sxs-lookup"><span data-stu-id="dcc66-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="dcc66-114">Значение элемента данных контента зависит от расположения структуры SkipBlock в серии и версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="dcc66-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="dcc66-115">Если первая структура SkipBlock не является завершающей, в Outlook рассматривается первая структура SkipBlock в качестве структуры потока [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) , указывающей имя поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="dcc66-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dcc66-116">См. также</span><span class="sxs-lookup"><span data-stu-id="dcc66-116">See also</span></span>



[<span data-ttu-id="dcc66-117">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="dcc66-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="dcc66-118">Структуры потока</span><span class="sxs-lookup"><span data-stu-id="dcc66-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="dcc66-119">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="dcc66-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="dcc66-120">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="dcc66-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

