---
title: Метод Append (коллекция Procedures в ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 838483d03ee57dd9a546692e130aea2360a5b83d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930618"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="75d91-102">Метод Append (коллекция Procedures в ADOX)</span><span class="sxs-lookup"><span data-stu-id="75d91-102">Append method (ADOX Procedures)</span></span>


<span data-ttu-id="75d91-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75d91-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="75d91-104">Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="75d91-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75d91-105">Syntax</span></span>

<span data-ttu-id="75d91-106">*Процедуры*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="75d91-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="75d91-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75d91-107">Parameters</span></span>

  - <span data-ttu-id="75d91-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="75d91-108">*Name*</span></span>

  - <span data-ttu-id="75d91-109">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="75d91-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="75d91-110">*Команда*</span><span class="sxs-lookup"><span data-stu-id="75d91-110">*Command*</span></span>

  - <span data-ttu-id="75d91-111">Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="75d91-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d91-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="75d91-112">Remarks</span></span>

<span data-ttu-id="75d91-113">Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="75d91-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="75d91-114">Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="75d91-114">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="75d91-115">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="75d91-115">**Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="75d91-116">При использовании поставщика OLE DB для Microsoft Jet, позволит метод **Append** коллекции **процедуры** можно использовать для определения **представления** , а не на **процедуру** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="75d91-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="75d91-117">**Представление** будет добавлен к источнику данных и добавляются в коллекцию **процедур** .</span><span class="sxs-lookup"><span data-stu-id="75d91-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="75d91-118">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** , **представление** больше не будет находиться в коллекции **процедуры** и будет отображаться в коллекции **представлений** .</span><span class="sxs-lookup"><span data-stu-id="75d91-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


