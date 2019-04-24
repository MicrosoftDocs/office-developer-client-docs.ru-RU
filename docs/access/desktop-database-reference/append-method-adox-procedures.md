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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297083"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="acc08-102">Метод Append (коллекция Procedures в ADOX)</span><span class="sxs-lookup"><span data-stu-id="acc08-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="acc08-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="acc08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="acc08-104">Добавляет новый объект [PROCEDURE](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="acc08-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acc08-105">Syntax</span></span>

<span data-ttu-id="acc08-106">*Процедуры*. *Имя*для добавления, *команда*</span><span class="sxs-lookup"><span data-stu-id="acc08-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="acc08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="acc08-107">Parameters</span></span>

|<span data-ttu-id="acc08-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="acc08-108">Parameter</span></span>|<span data-ttu-id="acc08-109">Описание</span><span class="sxs-lookup"><span data-stu-id="acc08-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="acc08-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="acc08-110">*Name*</span></span> |<span data-ttu-id="acc08-111">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="acc08-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="acc08-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="acc08-112">*Command*</span></span> |<span data-ttu-id="acc08-113">Объект [команды](command-object-ado.md) ADO, представляющий процедуру, которую необходимо создать и добавить.</span><span class="sxs-lookup"><span data-stu-id="acc08-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="acc08-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="acc08-114">Remarks</span></span>

<span data-ttu-id="acc08-115">Создает новую процедуру в источнике данных с именем и атрибутами, указанными в объекте **Command** .</span><span class="sxs-lookup"><span data-stu-id="acc08-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="acc08-116">Если текст команды, который указывает пользователь, представляет представление, а не процедуру, то поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="acc08-116">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="acc08-117">Если поставщик не поддерживает хранимые команды, **append** завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="acc08-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="acc08-118">При использовании поставщика OLE DB для Microsoft Jet метод **append** для коллекции **процедур** позволяет указать **представление** , а не **процедуру** в параметре *Command* .</span><span class="sxs-lookup"><span data-stu-id="acc08-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="acc08-119">**Представление** будет добавлено в источник данных и будет добавлено в коллекцию **процедур** .</span><span class="sxs-lookup"><span data-stu-id="acc08-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="acc08-120">После **добавления**, если коллекции **процедур** и **представлений** обновляются, **представление** больше не будет отображаться в коллекции **процедур** и будет отображаться в коллекции **views** .</span><span class="sxs-lookup"><span data-stu-id="acc08-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


