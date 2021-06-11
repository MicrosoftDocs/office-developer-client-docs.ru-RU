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
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="fd790-103">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="fd790-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="fd790-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd790-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd790-105">Структура потока PackedUnicodeString содержит представление строки Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="fd790-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="fd790-106">Эта строка не завершается null-символом.</span><span class="sxs-lookup"><span data-stu-id="fd790-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="fd790-107">Элементы данных в этом потоке хранятся в порядке маленького byte, сразу же следуя друг за другом в порядке, перечисленном ниже.</span><span class="sxs-lookup"><span data-stu-id="fd790-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="fd790-108">Фактические элементы данных, которые существуют, зависят от длины строки в представлении UTF-16.</span><span class="sxs-lookup"><span data-stu-id="fd790-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="fd790-109">Для строки, представление которой UTF-16 содержит менее 255 WCHARs, элементы данных представлены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fd790-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="fd790-110">Длина: BYTE (1 байт), длина в количестве WCHARs представления строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="fd790-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="fd790-111">Символы: массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="fd790-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="fd790-112">Количество этого массива равно элементу данных Length.</span><span class="sxs-lookup"><span data-stu-id="fd790-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="fd790-113">Данные в массиве — это представление строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="fd790-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="fd790-114">Для строки, представление которой UTF-16 содержит от 255 до 65535 WCHARs, элементы данных представлены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fd790-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="fd790-115">Префикс: BYTE (1 byte), значение 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="fd790-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="fd790-116">Длина: WORD (2 байта), длина в количестве WCHARs представления строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="fd790-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="fd790-117">Символы: массив WCHAR.</span><span class="sxs-lookup"><span data-stu-id="fd790-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="fd790-118">Количество этого массива равно элементу данных Length.</span><span class="sxs-lookup"><span data-stu-id="fd790-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="fd790-119">Данные в массиве — это представление строки UTF-16.</span><span class="sxs-lookup"><span data-stu-id="fd790-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd790-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fd790-120">See also</span></span>



[<span data-ttu-id="fd790-121">Outlook Элементы и поля</span><span class="sxs-lookup"><span data-stu-id="fd790-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="fd790-122">Структуры потока</span><span class="sxs-lookup"><span data-stu-id="fd790-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="fd790-123">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="fd790-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

