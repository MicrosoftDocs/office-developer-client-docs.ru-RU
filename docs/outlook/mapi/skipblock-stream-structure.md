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
# <a name="skipblock-stream-structure"></a><span data-ttu-id="85a78-103">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="85a78-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="85a78-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85a78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85a78-105">Структура потока SkipBlock — это блок данных, который начинается с integer, которое указывает длину оставшейся части блока.</span><span class="sxs-lookup"><span data-stu-id="85a78-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="85a78-106">Эта структура потока существует в [потоке FieldDefinition,](fielddefinition-stream-structure.md) если определение поля имеет формат PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="85a78-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="85a78-107">Назначение структуры потока SkipBlock зависит от его относительного расположения в ряду похожих структур в элементе данных SkipBlocks потока FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="85a78-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="85a78-108">Серия SkipBlocks должна содержать по крайней мере одну структуру SkipBlock, которая завершает ряд и имеет элемент данных Size, равный 0.</span><span class="sxs-lookup"><span data-stu-id="85a78-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="85a78-109">Если первая структура не является структурой прерывания (то есть элемент данных Size больше 0), Outlook предполагает, что первая структура указывает имя поля в Юникод (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="85a78-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="85a78-110">Элементы данных в этом потоке хранятся в порядок с небольшими конечными ветвями, сразу после друг друга в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="85a78-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="85a78-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span><span class="sxs-lookup"><span data-stu-id="85a78-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="85a78-112">Содержимое: массив BYTE.</span><span class="sxs-lookup"><span data-stu-id="85a78-112">Content: An array of BYTE.</span></span> <span data-ttu-id="85a78-113">Количество массивов равно элементу данных Size.</span><span class="sxs-lookup"><span data-stu-id="85a78-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="85a78-114">Значение элемента "Данные содержимого" зависит от расположения структуры SkipBlock в ряду и версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="85a78-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="85a78-115">Если первая структура SkipBlock не является структурой прерывания, Outlook рассматривает первую структуру SkipBlock как структуру [потока FirstSkipBlockContent,](firstskipblockcontent-stream-structure.md) которая указывает имя поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="85a78-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="85a78-116">См. также</span><span class="sxs-lookup"><span data-stu-id="85a78-116">See also</span></span>



[<span data-ttu-id="85a78-117">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="85a78-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="85a78-118">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="85a78-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="85a78-119">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="85a78-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="85a78-120">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="85a78-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

