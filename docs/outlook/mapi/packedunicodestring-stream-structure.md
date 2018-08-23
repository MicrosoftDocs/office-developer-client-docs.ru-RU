---
title: Структура потока PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569199"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="d919e-103">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="d919e-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="d919e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d919e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d919e-105">Структура потока PackedUnicodeString содержит представление Юникод (UTF-16) строки.</span><span class="sxs-lookup"><span data-stu-id="d919e-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="d919e-106">Эта строка не будет завершен символом null.</span><span class="sxs-lookup"><span data-stu-id="d919e-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="d919e-107">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="d919e-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="d919e-108">Фактические данные элементы, которые существуют зависят от длина строки в представление UTF-16.</span><span class="sxs-lookup"><span data-stu-id="d919e-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="d919e-109">Поиск строки, представление UTF-16 содержит меньше, чем 255 WCHARs элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d919e-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d919e-110">Продолжительность: БАЙТА (1 байт), длины, в число WCHARs, UTF-16-представления строки.</span><span class="sxs-lookup"><span data-stu-id="d919e-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="d919e-111">Символы: Массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d919e-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="d919e-112">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="d919e-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d919e-113">Данные в массиве — это представление UTF-16 строки.</span><span class="sxs-lookup"><span data-stu-id="d919e-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="d919e-114">Поиск строки, представление UTF-16 содержит WCHARs 255 до 65535 элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d919e-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="d919e-115">Префикс: БАЙТА (1 байт), значение 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="d919e-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="d919e-116">Продолжительность: WORD (2 байта), длины, в число WCHARs, UTF-16-представления строки.</span><span class="sxs-lookup"><span data-stu-id="d919e-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="d919e-117">Символы: Массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="d919e-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="d919e-118">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="d919e-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="d919e-119">Данные в массиве — это представление UTF-16 строки.</span><span class="sxs-lookup"><span data-stu-id="d919e-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d919e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d919e-120">See also</span></span>



[<span data-ttu-id="d919e-121">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="d919e-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="d919e-122">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="d919e-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d919e-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="d919e-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

