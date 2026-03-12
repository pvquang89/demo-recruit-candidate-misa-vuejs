<template>
  <!-- Main content area -->
  <div class="main-content commons-flex-1 commons-overflow-hidden commons-flex-col">
    <!-- Header Section -->
    <div class="content-header commons-flex-between">
      <h1 class="page-title commons-fs-20 commons-fw-700">Candidates</h1>
      <div class="header-actions commons-display-flex">
        <button
          class="btn-add-candidate commons-flex-center commons-color-white commons-border-none commons-fs-14 commons-fw-500 commons-pointer commons-transition-bg"
        >
          <span class="btn-icon icon-add-candidate"></span>
          <span>Add candidate</span>
        </button>
        <button
          class="btn-dropdown commons-flex-center-all commons-color-white commons-border-none commons-pointer commons-transition-bg"
        >
          <span class="dropdown-icon icon-down"></span>
        </button>
      </div>
    </div>

    <!-- Filter Section -->
    <div class="filter-section commons-flex-between commons-bg-white">
      <div class="search-box commons-flex-center commons-rounded-4 commons-bg-white">
        <span class="icon-ai-search-candidate"></span>
        <input
          type="text"
          placeholder="Quick Search or AI Assistant"
          class="filter-search-input commons-flex-1 commons-border-none commons-outline-none commons-fs-14"
        />
      </div>
      <div class="filter-actions commons-display-flex">
        <button
          class="filter-btn commons-flex-center-all commons-rounded-4 commons-bg-white commons-pointer commons-transition-bg"
        >
          <span class="icon-filter"></span>
        </button>
        <button
          class="filter-btn commons-flex-center-all commons-rounded-4 commons-bg-white commons-pointer commons-transition-bg"
        >
          <span class="icon-export"></span>
        </button>
        <button
          class="filter-btn commons-flex-center-all commons-rounded-4 commons-bg-white commons-pointer commons-transition-bg"
        >
          <span class="icon-interactive-history"></span>
        </button>
        <button
          class="filter-btn commons-flex-center-all commons-rounded-4 commons-bg-white commons-pointer commons-transition-bg"
        >
          <span class="icon-setting-column"></span>
        </button>
      </div>
    </div>

    <!-- Selection Toolbar (hidden by default) -->
    <div class="selection-toolbar commons-flex-between commons-bg-white">
      <div class="selection-info commons-flex-center">
        <span class="selection-count commons-fw-700">0</span>
        <span class="selection-text commons-fs-14">selecting</span>
        <a class="selection-deselect commons-pointer commons-fs-14">Deselect</a>
        <a class="selection-select-all commons-pointer commons-fs-14">Select all on the list</a>
      </div>
      <div class="selection-actions commons-flex-center">
        <button
          class="toolbar-btn commons-flex-center commons-pointer commons-border-none commons-bg-transparent"
        >
          <span class="icon-email"></span>
          <span class="commons-fs-14">Send email</span>
        </button>
        <button
          class="toolbar-btn commons-flex-center commons-pointer commons-border-none commons-bg-transparent"
        >
          <span class="icon-tag"></span>
          <span class="commons-fs-14">Manage tag</span>
        </button>
        <button
          class="toolbar-btn commons-flex-center commons-pointer commons-border-none commons-bg-transparent"
        >
          <span class="icon-task"></span>
          <span class="commons-fs-14">Create task</span>
        </button>
        <button
          class="toolbar-btn commons-flex-center commons-pointer commons-border-none commons-bg-transparent"
        >
          <span class="icon-campaign"></span>
          <span class="commons-fs-14">Add to campaign</span>
        </button>
        <button
          class="toolbar-btn toolbar-btn-delete commons-flex-center commons-pointer commons-border-none commons-bg-transparent"
        >
          <span class="icon-delete" style="width: 20px; height: 20px"></span>
          <span class="commons-fs-14">Delete</span>
        </button>
      </div>
    </div>

    <!-- Table Section -->
    <div class="table-container commons-flex-1 commons-overflow-hidden commons-flex-col">
      <div class="table-wrapper commons-flex-1 commons-overflow-auto">
        <table class="candidates-table commons-w-full commons-fs-14">
          <thead>
            <tr>
              <th class="col-checkbox"><input type="checkbox" /></th>
              <th class="col-fullname commons-fw-700 commons-text-left commons-text-nowrap">
                Full name
              </th>
              <th class="col-email commons-fw-700 commons-text-left commons-text-nowrap">Email</th>
              <th class="col-phone commons-fw-700 commons-text-left commons-text-nowrap">
                Phone number
              </th>
              <th class="col-campaign commons-fw-700 commons-text-left commons-text-nowrap">
                Recruitment campaign
              </th>
              <th class="col-position commons-fw-700 commons-text-left commons-text-nowrap">
                Recruiting position
              </th>
              <th class="col-jobs commons-fw-700 commons-text-left commons-text-nowrap">Jobs</th>
              <th class="col-round commons-fw-700 commons-text-left commons-text-nowrap">
                Recruitment round
              </th>
              <th class="col-review commons-fw-700 commons-text-left commons-text-nowrap">
                Review
              </th>
              <th class="col-appdate commons-fw-700 commons-text-left commons-text-nowrap">
                Application date
              </th>
              <th class="col-source commons-fw-700 commons-text-left commons-text-nowrap">
                Candidate source
              </th>
              <th class="col-training commons-fw-700 commons-text-left commons-text-nowrap">
                Training level
              </th>
              <th class="col-place commons-fw-700 commons-text-left commons-text-nowrap">
                Training place
              </th>
              <th class="col-major commons-fw-700 commons-text-left commons-text-nowrap">Major</th>
              <th class="col-workplace commons-fw-700 commons-text-left commons-text-nowrap">
                Recent Workplace
              </th>
              <th class="col-recommend commons-fw-700 commons-text-left commons-text-nowrap">
                Recommending staff
              </th>
              <th class="col-department commons-fw-700 commons-text-left commons-text-nowrap">
                Using department
              </th>
              <th class="col-compat commons-fw-700 commons-text-left commons-text-nowrap">
                Compatibility level
              </th>
              <th class="col-area commons-fw-700 commons-text-left commons-text-nowrap">Area</th>
              <th class="col-referral commons-fw-700 commons-text-left commons-text-nowrap">
                Referral
              </th>
              <th class="col-receipt commons-fw-700 commons-text-left commons-text-nowrap">
                Receipt information
              </th>
              <th class="col-talent commons-fw-700 commons-text-left commons-text-nowrap">
                In talent pool
              </th>
              <th class="col-portal commons-fw-700 commons-text-left commons-text-nowrap">
                Candidate portal account
              </th>
              <th class="col-tag commons-fw-700 commons-text-left commons-text-nowrap">Tag</th>
              <th class="col-status commons-fw-700 commons-text-left commons-text-nowrap">
                Status
              </th>
              <th class="col-sex commons-fw-700 commons-text-left commons-text-nowrap">Sex</th>
              <th class="col-dob commons-fw-700 commons-text-left commons-text-nowrap">
                Date of birth
              </th>
              <th class="col-address commons-fw-700 commons-text-left commons-text-nowrap">
                Address
              </th>
              <th class="col-reason commons-fw-700 commons-text-left commons-text-nowrap">
                Reason
              </th>
              <th class="col-collab commons-fw-700 commons-text-left commons-text-nowrap">
                Collaborators
              </th>
              <th class="col-receiptdate commons-fw-700 commons-text-left commons-text-nowrap">
                Receipt date
              </th>
              <th class="col-offer commons-fw-700 commons-text-left commons-text-nowrap">
                Job offer status
              </th>
              <th class="col-actions"></th>
            </tr>
          </thead>
          <tbody></tbody>
        </table>
      </div>
    </div>

    <!-- Pagination Section -->
    <div class="pagination-section commons-flex-between">
      <div class="total-records commons-fs-14">Total: <strong>0</strong> record</div>
      <div class="pagination-controls commons-flex-center">
        <span class="records-label commons-fs-14">Number of records/page</span>
        <select class="records-select commons-rounded-4 commons-fs-14 commons-pointer">
          <option value="25">25</option>
          <option value="50">50</option>
          <option value="100">100</option>
        </select>
        <span class="page-info commons-fs-14">1 - 2 record</span>
        <button
          class="page-btn prev commons-border-none commons-flex-center-all commons-fs-16"
          disabled
        >
          <div class="icon-left"></div>
        </button>
        <button class="page-btn next commons-border-none commons-flex-center-all commons-fs-16">
          <div class="icon-right"></div>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const candidates = ref([
  {
    id: 1,
    fullName: 'Nguyễn Văn An',
    email: 'an.nguyen@email.com',
    phone: '0912345678',
    campaign: 'IT Recruitment 2024',
    position: 'Senior Frontend Developer',
    jobs: 'FE-001',
    round: 'Technical Interview',
    review: 'Good',
    applicationDate: '2024-01-15',
    source: 'LinkedIn',
    trainingLevel: 'University',
    trainingPlace: 'Đại học Bách khoa Hà Nội',
    major: 'Computer Science',
    workplace: 'FPT Software',
    recommendingStaff: 'Trần Thị Bình',
    department: 'Technology',
    compatibilityLevel: '85%',
    area: 'Hà Nội',
    referral: 'Internal',
    receiptInfo: 'CV Received',
    inTalentPool: 'Yes',
    portalAccount: 'Active',
    tag: 'JavaScript, Vue.js',
    status: 'In Progress',
    sex: 'Male',
    dateOfBirth: '1995-06-15',
    address: 'Cầu Giấy, Hà Nội',
    reason: 'Career Growth',
    collaborators: 'HR Team',
    receiptDate: '2024-01-16',
    jobOfferStatus: 'Pending'
  },
  {
    id: 2,
    fullName: 'Trần Thị Mai',
    email: 'mai.tran@email.com',
    phone: '0923456789',
    campaign: 'Marketing Drive 2024',
    position: 'Digital Marketing Manager',
    jobs: 'MKT-002',
    round: 'HR Interview',
    review: 'Excellent',
    applicationDate: '2024-01-20',
    source: 'Company Website',
    trainingLevel: 'Master',
    trainingPlace: 'Đại học Kinh tế Quốc dân',
    major: 'Marketing',
    workplace: 'Vingroup',
    recommendingStaff: 'Lê Văn Cường',
    department: 'Marketing',
    compatibilityLevel: '92%',
    area: 'TP.HCM',
    referral: 'External',
    receiptInfo: 'Portfolio Received',
    inTalentPool: 'No',
    portalAccount: 'Active',
    tag: 'SEO, Content Marketing',
    status: 'Offer Extended',
    sex: 'Female',
    dateOfBirth: '1993-03-22',
    address: 'Quận 1, TP.HCM',
    reason: 'Better Opportunity',
    collaborators: 'Marketing Team',
    receiptDate: '2024-01-21',
    jobOfferStatus: 'Accepted'
  },
  {
    id: 3,
    fullName: 'Lê Hoàng Nam',
    email: 'nam.le@email.com',
    phone: '0934567890',
    campaign: 'Backend Developer Hunt',
    position: 'Backend Developer',
    jobs: 'BE-003',
    round: 'Coding Test',
    review: 'Good',
    applicationDate: '2024-02-01',
    source: 'VietnamWorks',
    trainingLevel: 'University',
    trainingPlace: 'Đại học Công nghệ - ĐHQGHN',
    major: 'Software Engineering',
    workplace: 'TMA Solutions',
    recommendingStaff: 'Phạm Thị Dung',
    department: 'Technology',
    compatibilityLevel: '78%',
    area: 'Đà Nẵng',
    referral: 'Internal',
    receiptInfo: 'CV Received',
    inTalentPool: 'Yes',
    portalAccount: 'Inactive',
    tag: 'Node.js, Python',
    status: 'Under Review',
    sex: 'Male',
    dateOfBirth: '1996-11-08',
    address: 'Hải Châu, Đà Nẵng',
    reason: 'New Challenge',
    collaborators: 'Tech Team',
    receiptDate: '2024-02-02',
    jobOfferStatus: 'Pending'
  },
  {
    id: 4,
    fullName: 'Phạm Thu Hà',
    email: 'ha.pham@email.com',
    phone: '0945678901',
    campaign: 'UI/UX Design Campaign',
    position: 'UI/UX Designer',
    jobs: 'DES-004',
    round: 'Portfolio Review',
    review: 'Outstanding',
    applicationDate: '2024-02-10',
    source: 'Behance',
    trainingLevel: 'University',
    trainingPlace: 'Đại học Kiến trúc Hà Nội',
    major: 'Industrial Design',
    workplace: 'Freelance',
    recommendingStaff: 'Nguyễn Văn Em',
    department: 'Design',
    compatibilityLevel: '95%',
    area: 'Hà Nội',
    referral: 'External',
    receiptInfo: 'Portfolio Received',
    inTalentPool: 'Yes',
    portalAccount: 'Active',
    tag: 'Figma, Adobe XD',
    status: 'Final Round',
    sex: 'Female',
    dateOfBirth: '1994-07-30',
    address: 'Đống Đa, Hà Nội',
    reason: 'Creative Environment',
    collaborators: 'Design Team',
    receiptDate: '2024-02-11',
    jobOfferStatus: 'Pending'
  },
  {
    id: 5,
    fullName: 'Đỗ Minh Quân',
    email: 'quan.do@email.com',
    phone: '0956789012',
    campaign: 'DevOps Recruitment 2024',
    position: 'DevOps Engineer',
    jobs: 'OPS-005',
    round: 'System Design',
    review: 'Excellent',
    applicationDate: '2024-02-15',
    source: 'GitHub',
    trainingLevel: 'University',
    trainingPlace: 'Đại học FPT',
    major: 'Information Technology',
    workplace: 'VNG Corporation',
    recommendingStaff: 'Trần Thị Giang',
    department: 'Infrastructure',
    compatibilityLevel: '88%',
    area: 'TP.HCM',
    referral: 'Internal',
    receiptInfo: 'GitHub Profile',
    inTalentPool: 'No',
    portalAccount: 'Active',
    tag: 'Docker, Kubernetes, AWS',
    status: 'Offer Extended',
    sex: 'Male',
    dateOfBirth: '1992-12-25',
    address: 'Bình Thạnh, TP.HCM',
    reason: 'Technical Growth',
    collaborators: 'DevOps Team',
    receiptDate: '2024-02-16',
    jobOfferStatus: 'Negotiating'
  }
])

const renderTableData = () => {
  const tbody = document.querySelector('.candidates-table tbody')
  if (!tbody) return

  tbody.innerHTML = candidates.value.map(candidate => `
    <tr>
      <td class="col-checkbox"><input type="checkbox" /></td>
      <td class="col-fullname">${candidate.fullName}</td>
      <td class="col-email">${candidate.email}</td>
      <td class="col-phone">${candidate.phone}</td>
      <td class="col-campaign">${candidate.campaign}</td>
      <td class="col-position">${candidate.position}</td>
      <td class="col-jobs">${candidate.jobs}</td>
      <td class="col-round">${candidate.round}</td>
      <td class="col-review">${candidate.review}</td>
      <td class="col-appdate">${candidate.applicationDate}</td>
      <td class="col-source">${candidate.source}</td>
      <td class="col-training">${candidate.trainingLevel}</td>
      <td class="col-place">${candidate.trainingPlace}</td>
      <td class="col-major">${candidate.major}</td>
      <td class="col-workplace">${candidate.workplace}</td>
      <td class="col-recommend">${candidate.recommendingStaff}</td>
      <td class="col-department">${candidate.department}</td>
      <td class="col-compat">${candidate.compatibilityLevel}</td>
      <td class="col-area">${candidate.area}</td>
      <td class="col-referral">${candidate.referral}</td>
      <td class="col-receipt">${candidate.receiptInfo}</td>
      <td class="col-talent">${candidate.inTalentPool}</td>
      <td class="col-portal">${candidate.portalAccount}</td>
      <td class="col-tag">${candidate.tag}</td>
      <td class="col-status">${candidate.status}</td>
      <td class="col-sex">${candidate.sex}</td>
      <td class="col-dob">${candidate.dateOfBirth}</td>
      <td class="col-address">${candidate.address}</td>
      <td class="col-reason">${candidate.reason}</td>
      <td class="col-collab">${candidate.collaborators}</td>
      <td class="col-receiptdate">${candidate.receiptDate}</td>
      <td class="col-offer">${candidate.jobOfferStatus}</td>
      <td class="col-actions">
        <button class="action-btn edit-btn" title="Edit">
          <span class="icon-edit"></span>
        </button>
        <button class="action-btn delete-btn" title="Delete">
          <span class="icon-delete"></span>
        </button>
      </td>
    </tr>
  `).join('')

  // Update total records
  const totalRecordsElement = document.querySelector('.total-records strong')
  if (totalRecordsElement) {
    totalRecordsElement.textContent = candidates.value.length
  }

  // Update page info
  const pageInfoElement = document.querySelector('.page-info')
  if (pageInfoElement) {
    pageInfoElement.textContent = `1 - ${candidates.value.length} record`
  }
}

onMounted(() => {
  renderTableData()
})
</script>
