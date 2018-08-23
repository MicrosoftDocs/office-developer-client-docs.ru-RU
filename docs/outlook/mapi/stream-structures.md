---
title: Структуры потоков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581582"
---
# <a name="stream-structures"></a><span data-ttu-id="48547-103">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="48547-103">Stream Structures</span></span>

  
  
<span data-ttu-id="48547-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48547-105">Определения пользовательских полей элемента Microsoft Outlook сохраняются в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="48547-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="48547-106">Значение этого свойства — это двоичный поток, который содержит определения пользовательских полей и параметров привязки данных для встроенных полей для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="48547-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="48547-107">В этом разделе представлены сведения о структуре двоичный поток, разбитым в следующих структур потока.</span><span class="sxs-lookup"><span data-stu-id="48547-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="48547-108">Имена эти структуры потока (например, определение свойства, FieldDefinition и SkipBlock) и их элементов данных не технически частью API-интерфейс системы обмена сообщениями API (MAPI) и содержащиеся в этой статье только для документации в целях структур фактический потока.</span><span class="sxs-lookup"><span data-stu-id="48547-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="48547-109">Разработчики можно пометить эти элементы структуры и данные потока в своих приложениях по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="48547-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="48547-110">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="48547-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="48547-111">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="48547-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="48547-112">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="48547-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="48547-113">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="48547-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="48547-114">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="48547-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="48547-115">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="48547-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="48547-116">См. также</span><span class="sxs-lookup"><span data-stu-id="48547-116">See also</span></span>



[<span data-ttu-id="48547-117">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="48547-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="48547-118">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="48547-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="48547-119">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="48547-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

