---
title: Макрокоманда LockNavigationPane
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717806"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="85246-102">Макрокоманда LockNavigationPane</span><span class="sxs-lookup"><span data-stu-id="85246-102">LockNavigationPane macro action</span></span>


<span data-ttu-id="85246-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85246-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85246-104">Чтобы запретить пользователям удалять объекты базы данных, которые отображаются в области навигации можно использовать действие **LockNavigationPane** .</span><span class="sxs-lookup"><span data-stu-id="85246-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="85246-105">Setting</span><span class="sxs-lookup"><span data-stu-id="85246-105">Setting</span></span>

<span data-ttu-id="85246-106">Действие **LockNavigationPane** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="85246-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85246-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="85246-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="85246-108">Описание</span><span class="sxs-lookup"><span data-stu-id="85246-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85246-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="85246-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="85246-110">Выберите <strong>Да</strong> для блокировки области переходов или <strong>Нет</strong> для разблокировки области навигации.</span><span class="sxs-lookup"><span data-stu-id="85246-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="85246-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="85246-111">Remarks</span></span>

<span data-ttu-id="85246-112">Закрепление области переходов позволяет удалять объекты базы данных или обрезка объектов базы данных в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="85246-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="85246-113">Оно делает это *не* препятствует выполнению любой из следующих операций:</span><span class="sxs-lookup"><span data-stu-id="85246-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="85246-114">Копирование объектов базы данных в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="85246-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="85246-115">Вставка объектов базы данных из буфера обмена</span><span class="sxs-lookup"><span data-stu-id="85246-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="85246-116">Отображение или скрытие области переходов</span><span class="sxs-lookup"><span data-stu-id="85246-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="85246-117">Выбор другой схемы организации области переходов</span><span class="sxs-lookup"><span data-stu-id="85246-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="85246-118">Отображение или скрытие разделов области переходов</span><span class="sxs-lookup"><span data-stu-id="85246-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="85246-119">Чтобы выполнить действие **LockNavigationPane** в модуле VBA, используйте метод **LockNavigationPane** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="85246-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

