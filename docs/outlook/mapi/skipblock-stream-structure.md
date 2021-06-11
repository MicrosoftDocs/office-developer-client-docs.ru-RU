---
title: Структура skipBlock Stream
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
# <a name="skipblock-stream-structure"></a><span data-ttu-id="d82ba-103">Структура skipBlock Stream</span><span class="sxs-lookup"><span data-stu-id="d82ba-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="d82ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d82ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d82ba-105">Структура потока SkipBlock — это блок данных, который начинается с integer, который указывает длину оставшейся части блока.</span><span class="sxs-lookup"><span data-stu-id="d82ba-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="d82ba-106">Эта структура потока существует в [потоке FieldDefinition,](fielddefinition-stream-structure.md) если определение поля находится в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="d82ba-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="d82ba-107">Назначение структуры потока SkipBlock зависит от его относительного расположения в серии похожих структур в элементе данных SkipBlocks потока FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="d82ba-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="d82ba-108">Серия SkipBlocks должна содержать по крайней мере одну структуру SkipBlock, которая завершает серию и имеет элемент данных Size, равный 0.</span><span class="sxs-lookup"><span data-stu-id="d82ba-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="d82ba-109">Если первая структура не является структурой прекращения (то есть элемент данных Size больше 0), Outlook предполагает, что первая структура указывает имя поля в Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="d82ba-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="d82ba-110">Элементы данных в этом потоке хранятся в порядке маленького byte, немедленно следуя друг за другом в порядке, указанном ниже.</span><span class="sxs-lookup"><span data-stu-id="d82ba-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="d82ba-111">Размер: DWORD (4 bytes), размер, в количестве bytes, элемента данных контента.</span><span class="sxs-lookup"><span data-stu-id="d82ba-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="d82ba-112">Содержимое. Массив BYTE.</span><span class="sxs-lookup"><span data-stu-id="d82ba-112">Content: An array of BYTE.</span></span> <span data-ttu-id="d82ba-113">Количество этого массива равно элементу Данных Size.</span><span class="sxs-lookup"><span data-stu-id="d82ba-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="d82ba-114">Значение элемента данных контента зависит от расположения структуры SkipBlock в серии и версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="d82ba-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="d82ba-115">Если первая структура SkipBlock не является структурой прекращения, Outlook первой структурой SkipBlock является структура [потока FirstSkipBlockContent,](firstskipblockcontent-stream-structure.md) которая указывает имя поля в Unicode.</span><span class="sxs-lookup"><span data-stu-id="d82ba-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d82ba-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d82ba-116">See also</span></span>



[<span data-ttu-id="d82ba-117">Outlook Элементы и поля</span><span class="sxs-lookup"><span data-stu-id="d82ba-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="d82ba-118">Структуры потока</span><span class="sxs-lookup"><span data-stu-id="d82ba-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d82ba-119">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="d82ba-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="d82ba-120">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="d82ba-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

