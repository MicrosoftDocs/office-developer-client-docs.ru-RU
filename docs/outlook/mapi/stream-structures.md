---
title: Структуры потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407825"
---
# <a name="stream-structures"></a><span data-ttu-id="8b835-103">Структуры потока</span><span class="sxs-lookup"><span data-stu-id="8b835-103">Stream Structures</span></span>

  
  
<span data-ttu-id="8b835-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b835-105">Определения определяемых пользователем полей элемента Microsoft Outlook хранятся в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8b835-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="8b835-106">Значение этого свойства — это двоичный поток, который содержит определения пользовательских полей и параметры привязки к данным для встроенных полей элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="8b835-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="8b835-107">В этом разделе представлены сведения о структуре двоичного потока, разбитых в следующих структурах потока.</span><span class="sxs-lookup"><span data-stu-id="8b835-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b835-108">Имена этих структур потоков (например, PropertyDefinition, FieldDefinition и SkipBlock) и их элементы данных технически не являются частью программного интерфейса API обмена сообщениями (MAPI) и предоставляются здесь только для документации. для фактических структур потоков.</span><span class="sxs-lookup"><span data-stu-id="8b835-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="8b835-109">Разработчики могут помечать эти структуры потоков и элементы данных в своих приложениях по мере их выбора.</span><span class="sxs-lookup"><span data-stu-id="8b835-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="8b835-110">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="8b835-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="8b835-111">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="8b835-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="8b835-112">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="8b835-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="8b835-113">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="8b835-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="8b835-114">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="8b835-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="8b835-115">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="8b835-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="8b835-116">См. также</span><span class="sxs-lookup"><span data-stu-id="8b835-116">See also</span></span>



[<span data-ttu-id="8b835-117">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="8b835-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="8b835-118">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="8b835-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="8b835-119">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="8b835-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

