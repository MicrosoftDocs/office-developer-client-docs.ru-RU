---
title: Структура потока PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422616"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="c30b7-103">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="c30b7-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="c30b7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c30b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c30b7-105">Структура потока PackedUnicodeString содержит представление строки в коде Юникода (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="c30b7-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="c30b7-106">Эта строка не завершается символом NULL.</span><span class="sxs-lookup"><span data-stu-id="c30b7-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="c30b7-107">Элементы данных в этом потоке хранятся в порядке с небольшим набором элементов, сразу же после друг друга в порядке, приведенном ниже.</span><span class="sxs-lookup"><span data-stu-id="c30b7-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="c30b7-108">Фактические элементы данных зависят от длины строки в представлении UTF-16.</span><span class="sxs-lookup"><span data-stu-id="c30b7-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="c30b7-109">Для строки, представление UTF-16 которой содержит менее 255 WCHARs, элементы данных:</span><span class="sxs-lookup"><span data-stu-id="c30b7-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="c30b7-110">Длина: БАЙТ (1 байт), длина (в количестве WCHARs) представления строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="c30b7-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="c30b7-111">Символы: массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="c30b7-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="c30b7-112">Количество массивов равно элементу данных Length.</span><span class="sxs-lookup"><span data-stu-id="c30b7-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="c30b7-113">Данные в массиве — это представление строки в UTF-16.</span><span class="sxs-lookup"><span data-stu-id="c30b7-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="c30b7-114">Для строки, представление UTF-16 которой содержит от 255 до 65535 WCHARs, элементы данных:</span><span class="sxs-lookup"><span data-stu-id="c30b7-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="c30b7-115">Префикс: BYTE (1 byte), значение 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="c30b7-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="c30b7-116">Длина: WORD (2 байта), длина (в количестве WCHARs) представления строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="c30b7-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="c30b7-117">Символы: массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="c30b7-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="c30b7-118">Количество массивов равно элементу данных Length.</span><span class="sxs-lookup"><span data-stu-id="c30b7-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="c30b7-119">Данные в массиве — это представление строки в UTF-16.</span><span class="sxs-lookup"><span data-stu-id="c30b7-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c30b7-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c30b7-120">See also</span></span>



[<span data-ttu-id="c30b7-121">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="c30b7-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="c30b7-122">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="c30b7-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="c30b7-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="c30b7-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

