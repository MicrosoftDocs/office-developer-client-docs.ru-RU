---
title: Метод Append (коллекция Procedures в ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65a8e0b805bf964ae60bd9de25fc45cf5b04482f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949693"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="ba5ac-102">Метод Append (коллекция Procedures в ADOX)</span><span class="sxs-lookup"><span data-stu-id="ba5ac-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="ba5ac-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba5ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba5ac-104">Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ba5ac-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba5ac-105">Syntax</span></span>

<span data-ttu-id="ba5ac-106">*Процедуры*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="ba5ac-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="ba5ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba5ac-107">Parameters</span></span>

|<span data-ttu-id="ba5ac-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="ba5ac-108">Parameter</span></span>|<span data-ttu-id="ba5ac-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ba5ac-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ba5ac-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="ba5ac-110">*Name*</span></span> |<span data-ttu-id="ba5ac-111">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="ba5ac-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="ba5ac-112">*Команда*</span><span class="sxs-lookup"><span data-stu-id="ba5ac-112">*Command*</span></span> |<span data-ttu-id="ba5ac-113">Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="ba5ac-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ba5ac-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba5ac-114">Remarks</span></span>

<span data-ttu-id="ba5ac-115">Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="ba5ac-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="ba5ac-116">Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="ba5ac-116">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="ba5ac-117">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="ba5ac-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="ba5ac-118">При использовании поставщика OLE DB для Microsoft Jet, позволит метод **Append** коллекции **процедуры** можно использовать для определения **представления** , а не на **процедуру** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="ba5ac-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="ba5ac-119">**Представление** будет добавлен к источнику данных и добавляются в коллекцию **процедур** .</span><span class="sxs-lookup"><span data-stu-id="ba5ac-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="ba5ac-120">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** , **представление** больше не будет находиться в коллекции **процедуры** и будет отображаться в коллекции **представлений** .</span><span class="sxs-lookup"><span data-stu-id="ba5ac-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


