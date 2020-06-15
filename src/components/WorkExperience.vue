<template>
  <div class="work_experience">
    <div class="timeline">
      <div class="leftarrow">
        <svg
          width="10pt"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          xmlns="http://www.w3.org/2000/svg"
          height="10pt"
          viewBox="0 0 560 560"
        >
          <g
            transform="translate(0, -0.561)"
            style="fill:#2c3e50; fill-rule:evenodd; stroke:none; stroke-width:1; stroke-linecap:butt; stroke-linejoin:miter; stroke-dasharray:none;"
          >
            <path
              d="M0 559.991 C0 558.504 279.994 0 280.458 0.561456 C282.014 2.44528 560.512 560.13 559.999 560.337 C559.665 560.472 496.562 533.384 419.77 500.142 C419.77 500.142 280.15 439.701 280.15 439.701 C280.15 439.701 140.756 500.131 140.756 500.131 C64.0894 533.368 1.05572 560.561 0.681114 560.561 C0.306506 560.561 8e-06 560.304 8e-06 559.991 C8e-06 559.991 0 559.991 0 559.991 Z"
            />
          </g>
        </svg>
      </div>
      <div class="line"></div>
      <div class="rightarrow">
        <svg
          width="10pt"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          xmlns="http://www.w3.org/2000/svg"
          height="10pt"
          viewBox="0 0 560 560"
        >
          <g
            transform="translate(0, -0.561)"
            style="fill:#2c3e50; fill-rule:evenodd; stroke:none; stroke-width:1; stroke-linecap:butt; stroke-linejoin:miter; stroke-dasharray:none;"
          >
            <path
              d="M0 559.991 C0 558.504 279.994 0 280.458 0.561456 C282.014 2.44528 560.512 560.13 559.999 560.337 C559.665 560.472 496.562 533.384 419.77 500.142 C419.77 500.142 280.15 439.701 280.15 439.701 C280.15 439.701 140.756 500.131 140.756 500.131 C64.0894 533.368 1.05572 560.561 0.681114 560.561 C0.306506 560.561 8e-06 560.304 8e-06 559.991 C8e-06 559.991 0 559.991 0 559.991 Z"
            />
          </g>
        </svg>
      </div>
      <div class="jobs">
        <JobItem
          v-for="job in widthAdjustedJobs"
          :key="job.employer"
          :employer="job.employer"
          :year="job.year"
          :title="job.title"
          :logo="job.logo"
        />
      </div>
    </div>
    <div class="mobile_timeline">
      <MobileJobItem
        v-for="job in jobs"
        :key="job.employer"
        :employer="job.employer"
        :title="job.title"
        :logo="job.logo"
        :startDate="job.startDate"
        :endDate="job.endDate"
      />
    </div>
  </div>
</template>

<script>
import JobItem from "./JobItem.vue";
import MobileJobItem from "./MobileJobItem.vue";

export default {
  name: "WorkExperience",
  components: {
    JobItem,
    MobileJobItem,
  },
  data() {
    return {
      jobs: [
        {
          employer: "TechJect",
          title: "Intern",
          year: "2015",
          startDate: "May 2015",
          endDate: "July 2015",
          logo: "techject.jpg",
        },
        {
          employer: "Automation Direct",
          title: "Intern",
          year: "2016",
          startDate: "May 2016",
          endDate: "July 2016",
          logo: "automationdirect.png",
        },
        {
          employer: "Ultic Web Solutions",
          title: "Founder",
          year: "2017",
          startDate: "Feb 2017",
          endDate: "Feb 2019",
          logo: "ultic.png",
        },
        {
          employer: "Emory University",
          title: "ION Research Scholar",
          year: "2017",
          startDate: "Jun 2017",
          endDate: "July 2017",
          logo: "emory.png",
        },
        {
          employer: "g.tec Neurotechnologies",
          title: "Research Scientist Intern",
          year: "2018",
          startDate: "May 2018",
          endDate: "Aug 2018",
          logo: "gtec.png",
        },
        {
          employer: "Brigham Young University",
          title: "Research Assistant",
          year: "2019",
          startDate: "Feb 2019",
          endDate: "Apr 2019",
          logo: "byu.png",
        },
        {
          employer: "Calibur",
          title: "Founder & CEO",
          year: "2020",
          startDate: "Jan 2019",
          endDate: "May 2020",
          logo: "calibur.png",
        },
      ],
    };
  },
  computed: {
    widthAdjustedJobs: function() {
      let width = window.innerWidth;
      if ((width < 1920) & (width >= 1300)) {
        return this.jobs.slice(2, 7);
      } else if ((width < 1300) & (width >= 421)) {
        return this.jobs.slice(4, 7);
      }
      return this.jobs;
    },
  },
};
</script>

<style>
.work_experience {
  width: 100%;
  height: 100%;
  background: #ffffff;
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.timeline {
  display: flex;
  width: 95%;
  height: 95%;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  position: relative;
}

.mobile_timeline {
  display: none;
}

.line {
  flex-grow: 3;
  border: 1px solid #2c3e50;
}

.leftarrow {
  transform: rotate(270deg);
  width: 14px;
  height: 14px;
}

.rightarrow {
  transform: rotate(90deg);
  width: 14px;
  height: 14px;
}
.jobs {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
}

@media screen and (max-width: 420px) {
  .work_experience {
    width: 100%;
    height: 100%;
  }

  .timeline,
  .jobs {
    display: none;
  }

  .mobile_timeline {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    justify-content: start;
  }
}
</style>
