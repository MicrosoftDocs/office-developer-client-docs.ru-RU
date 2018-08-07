---
title: Структура потока PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810084"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="d9f98-103">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="d9f98-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="d9f98-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9f98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9f98-105">Структура потока PackedAnsiString содержит представление в формате ANSI строку, основанную на кодовая страница ANSI компьютера, на котором выполняется Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="d9f98-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="d9f98-106">Эта строка не будет завершен символом null.</span><span class="sxs-lookup"><span data-stu-id="d9f98-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="d9f98-107">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="d9f98-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="d9f98-108">Фактические данные элементы, которые существуют зависят от длина строки в кодировке ANSI представление.</span><span class="sxs-lookup"><span data-stu-id="d9f98-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="d9f98-109">Поиск строки, представление ANSI содержит меньше, чем 255 байт элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9f98-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d9f98-110">Продолжительность: БАЙТА (1 байт), длина, в байтах, ANSI-представления строки.</span><span class="sxs-lookup"><span data-stu-id="d9f98-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="d9f98-111">Символы: Массив символов.</span><span class="sxs-lookup"><span data-stu-id="d9f98-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="d9f98-112">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="d9f98-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d9f98-113">Данные в массиве является представлением ANSI строки.</span><span class="sxs-lookup"><span data-stu-id="d9f98-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="d9f98-114">Поиск строки, представление ANSI содержит 255 до 65535 байт элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9f98-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d9f98-115">Префикс: БАЙТА (1 байт), значение 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="d9f98-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="d9f98-116">Продолжительность: WORD (2 байта), длина, в байтах, ANSI-представления строки.</span><span class="sxs-lookup"><span data-stu-id="d9f98-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="d9f98-117">Символы: Массив символов.</span><span class="sxs-lookup"><span data-stu-id="d9f98-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="d9f98-118">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="d9f98-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d9f98-119">Данные в массиве является представлением ANSI строки.</span><span class="sxs-lookup"><span data-stu-id="d9f98-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9f98-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d9f98-120">See also</span></span>



[<span data-ttu-id="d9f98-121">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="d9f98-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="d9f98-122">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="d9f98-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d9f98-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="d9f98-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

