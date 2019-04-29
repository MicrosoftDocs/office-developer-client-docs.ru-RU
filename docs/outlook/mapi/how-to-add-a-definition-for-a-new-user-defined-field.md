---
title: Добавление определения для нового пользовательского поля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428167"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="e9124-103">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="e9124-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="e9124-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9124-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9124-105">При добавлении поля, определенного пользователем, в элемент Microsoft Outlook вы добавляете определение поля в соответствующую структуру потока [PropertyDefinition](propertydefinition-stream-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e9124-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="e9124-106">Используйте следующую процедуру для добавления нового определения поля в структуру потока PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e9124-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="e9124-107">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="e9124-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="e9124-108">Скопируйте существующие определения полей структуры потока PropertyDefinition в новый массив определений полей.</span><span class="sxs-lookup"><span data-stu-id="e9124-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="e9124-109">Если существующие определения полей находятся в формате PropDefV1, преобразуйте их в формат PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="e9124-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="e9124-110">Дополнительные сведения о форматах определений полей приведены в разделе [структура потока PropertyDefinition](propertydefinition-stream-structure.md) и [структура потока FieldDefinition](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e9124-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="e9124-111">Создайте определение нового определяемого пользователем поля в формате PropDefV2 и добавьте его в массив.</span><span class="sxs-lookup"><span data-stu-id="e9124-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="e9124-112">ПриСвойте элементу Version структуры потока PropertyDefinition значение 0x0103, если для элемента Version не задано это значение.</span><span class="sxs-lookup"><span data-stu-id="e9124-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="e9124-113">Увеличьте значение элемента Фиелддефинитионкаунт на 1.</span><span class="sxs-lookup"><span data-stu-id="e9124-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="e9124-114">Сохраните массив в качестве значения элемента Фиелддефинитионс.</span><span class="sxs-lookup"><span data-stu-id="e9124-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9124-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e9124-115">See also</span></span>

- [<span data-ttu-id="e9124-116">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="e9124-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

