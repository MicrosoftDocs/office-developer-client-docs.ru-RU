---
title: Добавьте определение для нового пользовательского поля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592719"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="50c8e-103">Добавьте определение для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="50c8e-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="50c8e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c8e-105">При добавлении пользовательских полей в элемент Microsoft Outlook вы добавьте определение поля в соответствующем структуру потока [Определение свойства](propertydefinition-stream-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="50c8e-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="50c8e-106">Используйте следующую процедуру, чтобы добавить новое определение поля на структуру потока определение свойства.</span><span class="sxs-lookup"><span data-stu-id="50c8e-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="50c8e-107">Добавление определения пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="50c8e-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="50c8e-108">Копирование существующего определения полей структуры потока определение свойства новый массив определения поля.</span><span class="sxs-lookup"><span data-stu-id="50c8e-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="50c8e-109">Если все существующие определения поля, в формате PropDefV1 преобразуйте их в формат PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="50c8e-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="50c8e-110">Дополнительные сведения о форматах определения поля [Определение свойства потока](propertydefinition-stream-structure.md) - [Структура потока FieldDefinition](fielddefinition-stream-structure.md)см.</span><span class="sxs-lookup"><span data-stu-id="50c8e-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="50c8e-111">Создание определения нового поля, выбранные пользователем в формате PropDefV2 и добавить его в массиве.</span><span class="sxs-lookup"><span data-stu-id="50c8e-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="50c8e-112">Установите элемент Version структуры потока определение свойства в качестве 0x0103, если элемент Version не были установлены для этого значения.</span><span class="sxs-lookup"><span data-stu-id="50c8e-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="50c8e-113">Увеличьте элемент FieldDefinitionCount на 1.</span><span class="sxs-lookup"><span data-stu-id="50c8e-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="50c8e-114">Сохраните как значение элемента FieldDefinitions массива.</span><span class="sxs-lookup"><span data-stu-id="50c8e-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50c8e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="50c8e-115">See also</span></span>

- [<span data-ttu-id="50c8e-116">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="50c8e-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

