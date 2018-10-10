---
title: UpdateRule Property (ADOX)
TOCTitle: UpdateRule Property (ADOX)
ms:assetid: edefa80a-b83b-e811-996c-6f0318722c84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250206(v=office.15)
ms:contentKeyID: 48548548
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8bdb05dd1c7a16077cfa47c7791b8169c6808aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483033"
---
# <a name="updaterule-property-adox"></a><span data-ttu-id="cb639-102">UpdateRule Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cb639-102">UpdateRule Property (ADOX)</span></span>


<span data-ttu-id="cb639-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb639-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb639-104">Указывает, то действие выполняется при обновлении первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="cb639-104">Indicates the action performed when a primary key is updated.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cb639-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cb639-105">Settings and Return Values</span></span>

<span data-ttu-id="cb639-106">Задает и возвращает значение типа **Long** , может быть одной из констант [RuleEnum](ruleenum.md) .</span><span class="sxs-lookup"><span data-stu-id="cb639-106">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants.</span></span> <span data-ttu-id="cb639-107">Значение по умолчанию — **adRINone**.</span><span class="sxs-lookup"><span data-stu-id="cb639-107">The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb639-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb639-108">Remarks</span></span>

<span data-ttu-id="cb639-109">Это свойство доступно только для чтения в объектах [ключ](key-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="cb639-109">This property is read-only on [Key](key-object-adox.md) objects already appended to the collection.</span></span>

