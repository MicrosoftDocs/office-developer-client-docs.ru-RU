---
title: Sessions
TOCTitle: Sessions
ms:assetid: d81121bb-5bf8-49fb-83c4-8d3a2ffeb978
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462099(v=office.15)
ms:contentKeyID: 55119890
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0e92afa830dc729d96a056987904967750d76fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351004"
---
# <a name="sessions"></a><span data-ttu-id="bbd53-102">Sessions</span><span class="sxs-lookup"><span data-stu-id="bbd53-102">Sessions</span></span>

<span data-ttu-id="bbd53-p101">В этом разделе приведен пример задачи, в которой используются сеансы Microsoft Outlook. Сеанс  это период времени, в течение которого пользователь находится в системе Outlook. В приложении Outlook сеанс представлен классом [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Этот класс поддерживает вход в приложение и выход из него, прямой доступ к объектам хранилища по идентификатору, прямой доступ к определенным папкам по умолчанию, а также доступ к источникам данных, владельцами которых являются другие пользователи. Поддерживаются только источники данных MAPI, которые обеспечивают доступ ко всем данным Outlook, хранящимся в почтовых хранилищах пользователя.</span><span class="sxs-lookup"><span data-stu-id="bbd53-p101">This section includes a sample task that pertains to Microsoft Outlook sessions. A session is a period of time during which a user logs on to Outlook. A session is represented in Outlook by the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) class. This class supports logging in and out, accessing storage objects directly by ID, accessing certain special default folders directly, and accessing data sources owned by other users. The only supported data source is MAPI, which allows access to all Outlook data stored in the user's mail stores.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bbd53-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bbd53-108">In this section</span></span>

|<span data-ttu-id="bbd53-109">Статья</span><span class="sxs-lookup"><span data-stu-id="bbd53-109">Topic</span></span>|<span data-ttu-id="bbd53-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bbd53-110">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="bbd53-111">Получение экземпляра Outlook и вход в него</span><span class="sxs-lookup"><span data-stu-id="bbd53-111">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)  |<span data-ttu-id="bbd53-112">В этой статье рассказано, как получить объект [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)), который представляет активный экземпляр Outlook, если один такой экземпляр уже работает на локальном компьютере, или создать экземпляр Outlook, выполнить вход в профиль, используемый по умолчанию, и возвратить этот экземпляр Outlook.</span><span class="sxs-lookup"><span data-stu-id="bbd53-112">Obtains an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Outlook, if there is one running on the local computer, or creates a new instance of Outlook, signs in to the default profile, and returns that instance of Outlook.</span></span>|

## <a name="see-also"></a><span data-ttu-id="bbd53-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bbd53-113">See also</span></span>

- [<span data-ttu-id="bbd53-114">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="bbd53-114">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

