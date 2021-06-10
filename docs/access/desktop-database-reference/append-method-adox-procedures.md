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
# <a name="append-method-adox-procedures"></a><span data-ttu-id="d6d12-102">Метод Append (коллекция Procedures в ADOX)</span><span class="sxs-lookup"><span data-stu-id="d6d12-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="d6d12-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6d12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6d12-104">Добавляет новый [объект Procedure](procedure-object-adox.md) в коллекцию [Procedures.](procedures-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="d6d12-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d12-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6d12-105">Syntax</span></span>

<span data-ttu-id="d6d12-106">*Процедуры*. Имя *приложения*, *команда*</span><span class="sxs-lookup"><span data-stu-id="d6d12-106">*Procedures*.Append *Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="d6d12-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6d12-107">Parameters</span></span>

|<span data-ttu-id="d6d12-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d6d12-108">Parameter</span></span>|<span data-ttu-id="d6d12-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d6d12-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d6d12-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="d6d12-110">*Name*</span></span> |<span data-ttu-id="d6d12-111">Значение **String,** которое указывает имя процедуры создания и приложения.</span><span class="sxs-lookup"><span data-stu-id="d6d12-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="d6d12-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="d6d12-112">*Command*</span></span> |<span data-ttu-id="d6d12-113">Объект ADO [Command,](command-object-ado.md) который представляет процедуру создания и приложения.</span><span class="sxs-lookup"><span data-stu-id="d6d12-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d6d12-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6d12-114">Remarks</span></span>

<span data-ttu-id="d6d12-115">Создает новую процедуру в источнике данных с именем и атрибутами, указанными в **объекте Command.**</span><span class="sxs-lookup"><span data-stu-id="d6d12-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="d6d12-116">Если указанный пользователем командный текст представляет представление, а не процедуру, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6d12-116">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="d6d12-117">**Приложение не** будет работать, если поставщик не поддерживает сохраняющиеся команды.</span><span class="sxs-lookup"><span data-stu-id="d6d12-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d12-118">При использовании поставщика OLE DB для  Microsoft Jet метод приложения коллекции процедур  позволит указать представление, а не процедуру в *параметре Command.*  </span><span class="sxs-lookup"><span data-stu-id="d6d12-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="d6d12-119">Представление **будет** добавлено в источник данных и будет добавлено в коллекцию **Процедур.**</span><span class="sxs-lookup"><span data-stu-id="d6d12-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="d6d12-120">После **приложения,** если  коллекции "Процедуры" и "Представления" будут обновлены, представление больше не будет в коллекции **Procedures** и будет отображаться в коллекции   **Views.**</span><span class="sxs-lookup"><span data-stu-id="d6d12-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


