---
title: CloseDatabase Macro Action
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483091"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="734b9-102">CloseDatabase Macro Action</span><span class="sxs-lookup"><span data-stu-id="734b9-102">CloseDatabase Macro Action</span></span>


<span data-ttu-id="734b9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="734b9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="734b9-104">Действие **CloseDatabase** можно использовать для закрытия текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="734b9-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="734b9-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="734b9-105">Setting</span></span>

<span data-ttu-id="734b9-106">Действие **CloseDatabase** не имеет каких-либо аргументов.</span><span class="sxs-lookup"><span data-stu-id="734b9-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="734b9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="734b9-107">Remarks</span></span>

  - <span data-ttu-id="734b9-108">Access не будут запускаться все действия, которые выполните действие **CloseDatabase** в макросе.</span><span class="sxs-lookup"><span data-stu-id="734b9-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="734b9-109">Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Закрыть базы данных**.</span><span class="sxs-lookup"><span data-stu-id="734b9-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="734b9-110">При наличии несохраненных объектов открыть при запуске действия **CloseDatabase** , диалоговых окон, которые отображаются такие же, как, отображаемые при нажатии кнопки **Закрыть базы данных**.</span><span class="sxs-lookup"><span data-stu-id="734b9-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="734b9-111">Чтобы выполнить действие **CloseDatabase** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseDatabase** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="734b9-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

