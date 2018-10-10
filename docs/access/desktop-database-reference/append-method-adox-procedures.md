---
title: Append Method (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480124"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="982d7-102">Append Method (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="982d7-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="982d7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="982d7-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="982d7-104">Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="982d7-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="982d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="982d7-105">Syntax</span></span>

<span data-ttu-id="982d7-106">*Процедуры*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="982d7-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="982d7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="982d7-107">Parameters</span></span>

  - <span data-ttu-id="982d7-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="982d7-108">*Name*</span></span>

  - <span data-ttu-id="982d7-109">**Строковое** значение, задающее имя процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="982d7-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="982d7-110">*Команда*</span><span class="sxs-lookup"><span data-stu-id="982d7-110">*Command*</span></span>

  - <span data-ttu-id="982d7-111">Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="982d7-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="982d7-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="982d7-112">Remarks</span></span>

<span data-ttu-id="982d7-113">Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="982d7-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="982d7-114">Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="982d7-114">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used.</span></span> <span data-ttu-id="982d7-115">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="982d7-115">**Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="982d7-116">При использовании поставщика OLE DB для Microsoft Jet, позволит метод <STRONG>Append</STRONG> коллекции <STRONG>процедуры</STRONG> можно использовать для определения <STRONG>представления</STRONG> , а не на <STRONG>процедуру</STRONG> с помощью параметра <EM>командной</EM> .</span><span class="sxs-lookup"><span data-stu-id="982d7-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="982d7-117"><STRONG>Представление</STRONG> будет добавлен к источнику данных и добавляются в коллекцию <STRONG>процедур</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="982d7-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="982d7-118">После <STRONG>добавления</STRONG>при обновлении семейств сайтов <STRONG>процедуры</STRONG> и <STRONG>представления</STRONG> , <STRONG>представление</STRONG> больше не будет находиться в коллекции <STRONG>процедуры</STRONG> и будет отображаться в коллекции <STRONG>представлений</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="982d7-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>


