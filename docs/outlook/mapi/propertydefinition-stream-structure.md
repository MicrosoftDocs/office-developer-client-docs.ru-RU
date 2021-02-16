---
title: Структура потока PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438591"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="455cd-103">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="455cd-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="455cd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="455cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="455cd-105">Структура потока PropertyDefinition — это массив структур [потока FieldDefinition,](fielddefinition-stream-structure.md) содержащий определения для всех пользовательских полей в элементе Microsoft Outlook, а также параметры привязки данных для некоторых встроенных полей.</span><span class="sxs-lookup"><span data-stu-id="455cd-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="455cd-106">Вы можете программным образом управлять структурой потока PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="455cd-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="455cd-107">Однако аналогичные результаты можно получить с помощью конструктора форм  Outlook и, в частности, диалоговое окно "Свойства" для привязанного к данным управления.</span><span class="sxs-lookup"><span data-stu-id="455cd-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="455cd-108">Определения полей в структуре потока PropertyDefinition могут иметь один из двух форматов: PropDefV1 и PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="455cd-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="455cd-109">Outlook поддерживает propDefV1 и PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="455cd-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="455cd-110">Все определения полей в одной структуре потока PropertyDefinition должны иметь одинаковый формат.</span><span class="sxs-lookup"><span data-stu-id="455cd-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="455cd-111">Дополнительные сведения о том, чем отличаются PropDefV1 и PropDefV2, см. в структуре [потока FieldDefinition.](fielddefinition-stream-structure.md)</span><span class="sxs-lookup"><span data-stu-id="455cd-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="455cd-112">Элементы данных в этом потоке хранятся в порядок с небольшими конечными ветвями, сразу после друг друга в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="455cd-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="455cd-113">Версия: WORD (2 bytes), формат определений полей в структуре потока PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="455cd-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="455cd-114">В следующей таблице представлены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="455cd-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="455cd-115">**Значение**</span><span class="sxs-lookup"><span data-stu-id="455cd-115">**Value**</span></span>|<span data-ttu-id="455cd-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="455cd-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="455cd-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="455cd-117">0x0102</span></span>  <br/> |<span data-ttu-id="455cd-118">Формат: PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="455cd-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="455cd-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="455cd-119">0x0103</span></span>  <br/> |<span data-ttu-id="455cd-120">Формат: PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="455cd-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="455cd-121">FieldDefinitionCount: DWORD (4 bytes), количество определений полей в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="455cd-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="455cd-122">Это количество элементов массива в элементе данных FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="455cd-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="455cd-123">FieldDefinitions: массив структур потока FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="455cd-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="455cd-124">Количество массивов равно элементу данных FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="455cd-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="455cd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="455cd-125">See also</span></span>

- [<span data-ttu-id="455cd-126">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="455cd-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="455cd-127">Добавление определения для нового поля User-Defined</span><span class="sxs-lookup"><span data-stu-id="455cd-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="455cd-128">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="455cd-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="455cd-129">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="455cd-129">Stream Structures</span></span>](stream-structures.md)

