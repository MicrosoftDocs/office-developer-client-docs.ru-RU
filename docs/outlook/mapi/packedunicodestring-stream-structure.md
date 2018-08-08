---
title: Структура потока PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810087"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="b4e33-103">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="b4e33-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="b4e33-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4e33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4e33-105">Структура потока PackedUnicodeString содержит представление Юникод (UTF-16) строки.</span><span class="sxs-lookup"><span data-stu-id="b4e33-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="b4e33-106">Эта строка не будет завершен символом null.</span><span class="sxs-lookup"><span data-stu-id="b4e33-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="b4e33-107">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="b4e33-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="b4e33-108">Фактические данные элементы, которые существуют зависят от длина строки в представление UTF-16.</span><span class="sxs-lookup"><span data-stu-id="b4e33-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="b4e33-109">Поиск строки, представление UTF-16 содержит меньше, чем 255 WCHARs элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4e33-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="b4e33-110">Продолжительность: БАЙТА (1 байт), длины, в число WCHARs, UTF-16-представления строки.</span><span class="sxs-lookup"><span data-stu-id="b4e33-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="b4e33-111">Символы: Массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="b4e33-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="b4e33-112">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="b4e33-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="b4e33-113">Данные в массиве — это представление UTF-16 строки.</span><span class="sxs-lookup"><span data-stu-id="b4e33-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="b4e33-114">Поиск строки, представление UTF-16 содержит WCHARs 255 до 65535 элементы данных, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4e33-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="b4e33-115">Префикс: БАЙТА (1 байт), значение 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="b4e33-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="b4e33-116">Продолжительность: WORD (2 байта), длины, в число WCHARs, UTF-16-представления строки.</span><span class="sxs-lookup"><span data-stu-id="b4e33-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="b4e33-117">Символы: Массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="b4e33-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="b4e33-118">Число этого массива равно элемент данных длины.</span><span class="sxs-lookup"><span data-stu-id="b4e33-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="b4e33-119">Данные в массиве — это представление UTF-16 строки.</span><span class="sxs-lookup"><span data-stu-id="b4e33-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4e33-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b4e33-120">See also</span></span>



[<span data-ttu-id="b4e33-121">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="b4e33-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="b4e33-122">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="b4e33-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="b4e33-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="b4e33-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

