---
title: Обзор поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433159"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="3299f-103">Обзор поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="3299f-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="3299f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3299f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3299f-105">Поставщик транспорта — это библиотека динамической компоновки (DLL), которая выступает в качестве посредника между подсистемой MAPI и одной или несколькими базовыми системами обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3299f-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="3299f-106">Система обмена сообщениями — это определенный механизм, с помощью которого отправляются и принимаются сообщения.</span><span class="sxs-lookup"><span data-stu-id="3299f-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="3299f-107">Вот некоторые примеры систем обмена сообщениями:</span><span class="sxs-lookup"><span data-stu-id="3299f-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="3299f-108">Общая сетевая файловая система, с которой поставщик транспорта записывает сообщения напрямую.</span><span class="sxs-lookup"><span data-stu-id="3299f-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="3299f-109">Сетевой интерфейс TCP/IP, который поставщик транспорта использует для подключения к серверу обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3299f-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="3299f-110">Веб-служба, к которой пользователи подключаются.</span><span class="sxs-lookup"><span data-stu-id="3299f-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="3299f-111">Система обмена сообщениями на основе ведущего приложения или системы автоматизации Office.</span><span class="sxs-lookup"><span data-stu-id="3299f-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="3299f-112">Набор вызовов удаленных процедур для сервера обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3299f-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="3299f-113">Все, что можно использовать для переноса данных с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="3299f-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="3299f-114">Библиотека DLL поставщика транспорта должна соответствовать интерфейсу, заданному MAPI.</span><span class="sxs-lookup"><span data-stu-id="3299f-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="3299f-115">Как разработчик поставщика транспорта вы реализуете этот интерфейс в терминах функций, присутствующих в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3299f-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

