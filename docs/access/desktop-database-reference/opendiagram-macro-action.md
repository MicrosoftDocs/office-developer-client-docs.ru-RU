---
title: Макрокоманда OpenDiagram
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288359"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="1f203-102">Макрокоманда OpenDiagram</span><span class="sxs-lookup"><span data-stu-id="1f203-102">OpenDiagram macro action</span></span>

<span data-ttu-id="1f203-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f203-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f203-104">В проекте Access можно использовать действие **OpenDiagram** для открытия схемы базы данных в представлении Design.</span><span class="sxs-lookup"><span data-stu-id="1f203-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="1f203-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="1f203-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="1f203-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="1f203-106">Setting</span></span>

<span data-ttu-id="1f203-107">Действие **OpenDiagram** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="1f203-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f203-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1f203-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1f203-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1f203-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f203-110"><strong>Имя схемы</strong></span><span class="sxs-lookup"><span data-stu-id="1f203-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1f203-111">Имя схемы базы данных для открытия.</span><span class="sxs-lookup"><span data-stu-id="1f203-111">The name of the database diagram to open.</span></span> <span data-ttu-id="1f203-112">Поле <strong>Имя диаграммы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все схемы базы данных в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1f203-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="1f203-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1f203-113">This is a required argument.</span></span> <span data-ttu-id="1f203-114">Если вы запустите макрос, содержащий действие <strong>OpenDiagram</strong> в базе данных библиотеки, Microsoft Access сначала ищет схему с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1f203-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="1f203-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f203-115">Remarks</span></span>

<span data-ttu-id="1f203-116">Это действие аналогично двойному нажатию диаграммы базы данных в области навигации или правой щелкнув диаграмму базы данных в области навигации, а затем щелкнув **Представление дизайна.**</span><span class="sxs-lookup"><span data-stu-id="1f203-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="1f203-117">Схему базы данных можно перетаскивать из области навигации в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="1f203-117">You can drag a database diagram from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="1f203-118">Это автоматически создает действие **OpenDiagram,** которое открывает схему базы данных в представлении Design.</span><span class="sxs-lookup"><span data-stu-id="1f203-118">This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="1f203-119">Чтобы выполнить **действие OpenDiagram** в Visual Basic для приложений (VBA), используйте метод **OpenDiagram** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="1f203-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

