---
title: Создание и использование идентификаторов записей в поставщиках хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437681"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="7795c-103">Создание и использование идентификаторов записей в поставщиках хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="7795c-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="7795c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7795c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7795c-105">Когда в хранилище сообщений создается новая папка или сообщение, поставщику store сообщений необходимо назначить этому объекту идентификатор записи, чтобы клиентские приложения могли ссылаться на него.</span><span class="sxs-lookup"><span data-stu-id="7795c-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="7795c-106">Поставщики хранимых сообщений могут либо повторно использовать несуществуют долгосрочные идентификаторы записей удаленных объектов, либо создавать новые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="7795c-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="7795c-107">Для поставщиков store сообщений нет требований; Однако, если это возможно, поставщик хранилище сообщений всегда должен создавать новые долгосрочные идентификаторы записей для новых объектов, а не повторно использовать старые.</span><span class="sxs-lookup"><span data-stu-id="7795c-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="7795c-108">Можно повторно использовать краткосрочные идентификаторы записей при удалении объектов, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="7795c-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="7795c-109">Причиной такого удаления является то, что клиенты могут кэшаторить идентификаторы записей, иногда в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="7795c-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="7795c-110">Если это произойдет, и поставщик store сообщений повторно будет использовать идентификаторы записей, идентификатор записи может ссылаться на другой объект, когда клиент открывает идентификатор записи, чем при первом получении идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="7795c-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="7795c-111">Если поставщик хранения сообщений не использует идентификаторы записей повторно или, по крайней мере, использует схему генерации идентификаторов записей, которая не повторяется в течение очень долгого времени, эта проблема не может возникнуть.</span><span class="sxs-lookup"><span data-stu-id="7795c-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="7795c-112">Аналогичным образом, поставщики store сообщений должны пытаться сохранить идентификаторы записей для папок и сообщений при их перемещении в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="7795c-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="7795c-113">Если поставщик хранения сообщений может сделать это, ссылки на объекты в хранилище не станут недопустимыми при перемещении объекта в другое расположение в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7795c-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7795c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="7795c-114">See also</span></span>

- [<span data-ttu-id="7795c-115">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="7795c-115">Message Store Features</span></span>](message-store-features.md)

