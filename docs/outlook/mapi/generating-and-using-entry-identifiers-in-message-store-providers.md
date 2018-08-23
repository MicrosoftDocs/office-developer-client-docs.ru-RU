---
title: Создание и использование идентификаторов запись в сообщении поставщиков хранилищ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565454"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="98956-103">Создание и использование идентификаторов запись в сообщении поставщиков хранилищ</span><span class="sxs-lookup"><span data-stu-id="98956-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="98956-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98956-105">При создании новой папки или сообщение в хранилище сообщений поставщика хранилища сообщений должен назначить идентификатор записи этот объект, таким образом, клиентские приложения можно ссылаться на него.</span><span class="sxs-lookup"><span data-stu-id="98956-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="98956-106">Поставщики хранилища сообщений можно повторно использовать нефункционирующие долгосрочного идентификаторы записей удаленных объектов или создать новые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="98956-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="98956-107">Не требуется одним из способов или другой для поставщиков хранилища сообщений; Тем не менее если это возможно, поставщика хранилища сообщений всегда следует создавать новые идентификаторы долгосрочного записей для новых объектов, а не повторное использование старых.</span><span class="sxs-lookup"><span data-stu-id="98956-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="98956-108">Дает возможность повторного использования краткосрочных идентификаторы записей при удалении объектов, которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="98956-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="98956-109">Для удаления объясняется, что клиенты могут кэшировать идентификаторы записей, в некоторых случаях для длительных периодов времени.</span><span class="sxs-lookup"><span data-stu-id="98956-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="98956-110">Если это происходит и поставщика хранилища сообщений повторного использования идентификаторы записей, существует возможность идентификатор записи для обращения к другой объект, когда клиент открывает идентификатор записи, чем при его сначала получить идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="98956-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="98956-111">Если поставщик хранения сообщения не повторного использования идентификаторы записей — или по крайней мере использует схему создания идентификатор записи, которая не повторяется для очень много времени, эта проблема не может возникнуть.</span><span class="sxs-lookup"><span data-stu-id="98956-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="98956-112">Аналогично поставщиков хранилища сообщений следует попытаться сохранить идентификаторы записей для папки и сообщения, когда они будут перенесены в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="98956-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="98956-113">Если поставщик хранения сообщений можно сделать, ссылки на объекты в хранилище будет становятся недействительными при перемещении объекта в другое место в хранилище.</span><span class="sxs-lookup"><span data-stu-id="98956-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98956-114">См. также</span><span class="sxs-lookup"><span data-stu-id="98956-114">See also</span></span>

- [<span data-ttu-id="98956-115">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="98956-115">Message Store Features</span></span>](message-store-features.md)

