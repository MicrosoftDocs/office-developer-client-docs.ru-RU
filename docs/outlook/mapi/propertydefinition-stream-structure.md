---
title: Определение свойства потока структуры
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812090"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="6e960-103">Определение свойства потока структуры</span><span class="sxs-lookup"><span data-stu-id="6e960-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="6e960-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e960-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e960-105">Структура потока определение свойства — массив структур [FieldDefinition](fielddefinition-stream-structure.md) потока, которые содержат определения для всех пользовательских полей в элемент Microsoft Outlook и параметры привязки данных для некоторых встроенных полей.</span><span class="sxs-lookup"><span data-stu-id="6e960-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="6e960-106">Можно программно работать структура потока определение свойства.</span><span class="sxs-lookup"><span data-stu-id="6e960-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="6e960-107">Тем не менее можно получить такой же результат с помощью конструктора форм Outlook, и, в частности, поле диалоговое окно **свойств** элемента управления с привязкой к данным.</span><span class="sxs-lookup"><span data-stu-id="6e960-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="6e960-108">Определения полей в структуре потока определение свойства может иметь одно из следующих форматов: PropDefV1 и PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="6e960-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="6e960-109">Outlook поддерживает PropDefV1 и PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="6e960-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="6e960-110">Все определения полей в структуре одного потока определение свойства должен иметь тот же формат.</span><span class="sxs-lookup"><span data-stu-id="6e960-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="6e960-111">Дополнительные сведения о отличия между PropDefV1 и PropDefV2 Просмотр [Структуры FieldDefinition потока](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="6e960-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="6e960-112">Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="6e960-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="6e960-113">Версия: WORD (2 байта), формат определения полей в определение свойства передать в потоковом режиме структуры.</span><span class="sxs-lookup"><span data-stu-id="6e960-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="6e960-114">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="6e960-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="6e960-115">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6e960-115">**Value**</span></span>|<span data-ttu-id="6e960-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e960-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="6e960-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="6e960-117">0x0102</span></span>  <br/> |<span data-ttu-id="6e960-118">Формат — PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="6e960-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="6e960-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="6e960-119">0x0103</span></span>  <br/> |<span data-ttu-id="6e960-120">Формат — PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="6e960-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="6e960-121">FieldDefinitionCount: Значение DWORD (4 байта), количество определения полей в этот поток.</span><span class="sxs-lookup"><span data-stu-id="6e960-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="6e960-122">Это число элементов массива в элементе data FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="6e960-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="6e960-123">FieldDefinitions: Массив структур FieldDefinition потока.</span><span class="sxs-lookup"><span data-stu-id="6e960-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="6e960-124">Число этого массива равно FieldDefinitionCount элемента данных.</span><span class="sxs-lookup"><span data-stu-id="6e960-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e960-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6e960-125">See also</span></span>

- [<span data-ttu-id="6e960-126">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="6e960-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="6e960-127">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="6e960-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="6e960-128">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="6e960-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="6e960-129">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="6e960-129">Stream Structures</span></span>](stream-structures.md)

