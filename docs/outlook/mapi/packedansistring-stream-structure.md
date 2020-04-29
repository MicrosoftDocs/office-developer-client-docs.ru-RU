---
title: Структура потока PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404507"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="279dc-103">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="279dc-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="279dc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="279dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="279dc-105">Структура потока PackedAnsiString содержит представление строки в кодировке ANSI на основе кодовой страницы ANSI компьютера, на котором работает Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="279dc-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="279dc-106">Эта строка не завершается символом NULL.</span><span class="sxs-lookup"><span data-stu-id="279dc-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="279dc-107">Элементы данных в этом потоке хранятся в порядке байтов с прямым порядком байтов, сразу после друг друга в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="279dc-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="279dc-108">Фактические элементы данных, которые существуют, зависят от длины строки в представлении ANSI.</span><span class="sxs-lookup"><span data-stu-id="279dc-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="279dc-109">Для строки, в которой представление ANSI содержит менее 255 байт, используются следующие элементы данных:</span><span class="sxs-lookup"><span data-stu-id="279dc-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="279dc-110">Length: BYTE (1 байт), длина (в байтах) представления строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="279dc-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="279dc-111">Символы: массив CHAR.</span><span class="sxs-lookup"><span data-stu-id="279dc-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="279dc-112">Количество этого массива равно элементу данных length.</span><span class="sxs-lookup"><span data-stu-id="279dc-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="279dc-113">Данные в массиве являются представлением строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="279dc-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="279dc-114">Для строки, в которой представление ANSI содержит 255 – 65535 байт, элементы данных выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="279dc-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="279dc-115">Префикс: BYTE (1 байт), значение 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="279dc-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="279dc-116">Length: WORD (2 байта), длина (в байтах) представления строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="279dc-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="279dc-117">Символы: массив CHAR.</span><span class="sxs-lookup"><span data-stu-id="279dc-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="279dc-118">Количество этого массива равно элементу данных length.</span><span class="sxs-lookup"><span data-stu-id="279dc-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="279dc-119">Данные в массиве являются представлением строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="279dc-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="279dc-120">См. также</span><span class="sxs-lookup"><span data-stu-id="279dc-120">See also</span></span>



[<span data-ttu-id="279dc-121">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="279dc-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="279dc-122">Структуры потока</span><span class="sxs-lookup"><span data-stu-id="279dc-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="279dc-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="279dc-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

