---
title: Добавьте метод (ADOX процедуры)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195cb08fb0b195b63cdddaa848554f24d028b498
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861878"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="98475-102">Добавьте метод (ADOX процедуры)</span><span class="sxs-lookup"><span data-stu-id="98475-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="98475-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98475-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="98475-104">Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="98475-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="98475-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98475-105">Syntax</span></span>

<span data-ttu-id="98475-106">*Процедуры*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="98475-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="98475-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98475-107">Parameters</span></span>

  - <span data-ttu-id="98475-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="98475-108">*Name*</span></span>

  - <span data-ttu-id="98475-109">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="98475-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="98475-110">*Команда*</span><span class="sxs-lookup"><span data-stu-id="98475-110">*Command*</span></span>

  - <span data-ttu-id="98475-111">Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="98475-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="98475-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="98475-112">Remarks</span></span>

<span data-ttu-id="98475-113">Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="98475-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="98475-114">Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="98475-114">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="98475-115">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="98475-115">**Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="98475-116">При использовании поставщика OLE DB для Microsoft Jet, позволит метод **Append** коллекции **процедуры** можно использовать для определения **представления** , а не на **процедуру** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="98475-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="98475-117">**Представление** будет добавлен к источнику данных и добавляются в коллекцию **процедур** .</span><span class="sxs-lookup"><span data-stu-id="98475-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="98475-118">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** , **представление** больше не будет находиться в коллекции **процедуры** и будет отображаться в коллекции **представлений** .</span><span class="sxs-lookup"><span data-stu-id="98475-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


