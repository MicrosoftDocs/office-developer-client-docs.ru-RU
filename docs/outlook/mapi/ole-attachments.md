---
title: �������� OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ccd4a77e74a4a4cbdfcd8474d4cc00d0d0516839
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584641"
---
# <a name="ole-attachments"></a><span data-ttu-id="b98ad-103">�������� OLE</span><span class="sxs-lookup"><span data-stu-id="b98ad-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="b98ad-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b98ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b98ad-p101">��������, ������� �������� ������� OLE, ���������� ��� ������� OLE 1 ����� ��� ����������� �������� �������������. ���� �������� ������ ������������� �������� �������� **IStorage** OLE 2, ������ ������ ���� ������������ � ����� OLE 1. ��� �������������� ����������� � ������� ������� **OleConvertIStorageToOLESTREAM**, ������� �������� ������ ���������� Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="b98ad-p101">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility. If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream. This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

