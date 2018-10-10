---
title: RestoreWindow Macro Action
TOCTitle: RestoreWindow Macro Action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1dc6776310b0544b8bb807327612637a5fbcff67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482729"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="c249d-102">RestoreWindow Macro Action</span><span class="sxs-lookup"><span data-stu-id="c249d-102">RestoreWindow Macro Action</span></span>


<span data-ttu-id="c249d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c249d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c249d-104">Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого или свернутого окна.</span><span class="sxs-lookup"><span data-stu-id="c249d-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c249d-105">Это действие не может применяться к windows кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c249d-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="c249d-106">Для получения сведений о действиях с кодом windows приведены в разделе свойство <STRONG>WindowState</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c249d-106">For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c249d-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="c249d-107">Setting</span></span>

<span data-ttu-id="c249d-108">Действие **RestoreWindow** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="c249d-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="c249d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="c249d-109">Remarks</span></span>

<span data-ttu-id="c249d-110">Это действие работает на выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="c249d-110">This action works on the selected object.</span></span> <span data-ttu-id="c249d-111">При свернутых объекта можно выбрать ее с помощью **ВыделитьОбъект** и последующее восстановление предыдущих размеров с помощью действия **RestoreWindow** .</span><span class="sxs-lookup"><span data-stu-id="c249d-111">If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="c249d-112">Чтобы переместить или изменить ее размер окна, после восстановления можно использовать действие **MoveAndSizeWindow** .</span><span class="sxs-lookup"><span data-stu-id="c249d-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="c249d-113">Действие **RestoreWindow** имеет тот же эффект, как нажать кнопку " **Восстановление** " в правом верхнем углу окна или выбрав команду **восстановить** в **элемент управления** меню.</span><span class="sxs-lookup"><span data-stu-id="c249d-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="c249d-114">Чтобы выполнить действие **RestoreWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **восстановления** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="c249d-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

