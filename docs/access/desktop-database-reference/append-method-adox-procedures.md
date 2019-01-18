---
title: Метод Append (коллекция Procedures в ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704849"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="2dd44-102">Метод Append (коллекция Procedures в ADOX)</span><span class="sxs-lookup"><span data-stu-id="2dd44-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="2dd44-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dd44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dd44-104">Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd44-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dd44-105">Syntax</span></span>

<span data-ttu-id="2dd44-106">*Процедуры*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="2dd44-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="2dd44-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2dd44-107">Parameters</span></span>

|<span data-ttu-id="2dd44-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2dd44-108">Parameter</span></span>|<span data-ttu-id="2dd44-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2dd44-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2dd44-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="2dd44-110">*Name*</span></span> |<span data-ttu-id="2dd44-111">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="2dd44-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="2dd44-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="2dd44-112">*Command*</span></span> |<span data-ttu-id="2dd44-113">Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="2dd44-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2dd44-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2dd44-114">Remarks</span></span>

<span data-ttu-id="2dd44-115">Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="2dd44-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="2dd44-116">Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="2dd44-116">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="2dd44-117">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="2dd44-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="2dd44-118">При использовании поставщика OLE DB для Microsoft Jet, позволит метод **Append** коллекции **процедуры** можно использовать для определения **представления** , а не на **процедуру** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="2dd44-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="2dd44-119">**Представление** будет добавлен к источнику данных и добавляются в коллекцию **процедур** .</span><span class="sxs-lookup"><span data-stu-id="2dd44-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="2dd44-120">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** , **представление** больше не будет находиться в коллекции **процедуры** и будет отображаться в коллекции **представлений** .</span><span class="sxs-lookup"><span data-stu-id="2dd44-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


