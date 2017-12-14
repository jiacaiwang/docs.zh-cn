---
title: "ICorProfilerCallback::RemotingServerReceivingMessage 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.RemotingServerReceivingMessage
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::RemotingServerReceivingMessage
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage method [.NET Framework profiling]
- RemotingServerReceivingMessage method [.NET Framework profiling]
ms.assetid: 5604d21f-e6b7-490e-b469-42122a7568e1
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5947541204edf7fd4359dfa3aca78ea62c8009c6
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackremotingserverreceivingmessage-method"></a><span data-ttu-id="2db9a-102">ICorProfilerCallback::RemotingServerReceivingMessage 方法</span><span class="sxs-lookup"><span data-stu-id="2db9a-102">ICorProfilerCallback::RemotingServerReceivingMessage Method</span></span>
<span data-ttu-id="2db9a-103">通知探查器进程已收到远程方法调用或激活请求。</span><span class="sxs-lookup"><span data-stu-id="2db9a-103">Notifies the profiler that the process has received a remote method invocation or activation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2db9a-104">语法</span><span class="sxs-lookup"><span data-stu-id="2db9a-104">Syntax</span></span>  
  
```  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2db9a-105">参数</span><span class="sxs-lookup"><span data-stu-id="2db9a-105">Parameters</span></span>  
 `pCookie`  
 <span data-ttu-id="2db9a-106">[in]中提供的值与一个值，将对应[icorprofilercallback:: Remotingclientsendingmessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md)在这些情况下：</span><span class="sxs-lookup"><span data-stu-id="2db9a-106">[in] A value that will correspond with the value provided in [ICorProfilerCallback::RemotingClientSendingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md) under these conditions:</span></span>  
  
-   <span data-ttu-id="2db9a-107">远程处理 GUID cookie 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="2db9a-107">Remoting GUID cookies are active.</span></span>  
  
-   <span data-ttu-id="2db9a-108">通道成功传输消息。</span><span class="sxs-lookup"><span data-stu-id="2db9a-108">The channel succeeds in transmitting the message.</span></span>  
  
-   <span data-ttu-id="2db9a-109">GUID cookie 上处于活动状态的客户端过程。</span><span class="sxs-lookup"><span data-stu-id="2db9a-109">GUID cookies are active on the client-side process.</span></span>  
  
 <span data-ttu-id="2db9a-110">这样的远程处理调用和逻辑调用堆栈的创建轻松配对。</span><span class="sxs-lookup"><span data-stu-id="2db9a-110">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="2db9a-111">[in]一个值，是`true`如果调用的是异步的; 否则为`false`。</span><span class="sxs-lookup"><span data-stu-id="2db9a-111">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2db9a-112">备注</span><span class="sxs-lookup"><span data-stu-id="2db9a-112">Remarks</span></span>  
 <span data-ttu-id="2db9a-113">如果消息请求是异步的能够使用任意线程将请求提供服务。</span><span class="sxs-lookup"><span data-stu-id="2db9a-113">If the message request is asynchronous, the request can be serviced by any arbitrary thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2db9a-114">要求</span><span class="sxs-lookup"><span data-stu-id="2db9a-114">Requirements</span></span>  
 <span data-ttu-id="2db9a-115">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2db9a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2db9a-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2db9a-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2db9a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2db9a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2db9a-118">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2db9a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2db9a-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2db9a-119">See Also</span></span>  
 [<span data-ttu-id="2db9a-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="2db9a-120">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)